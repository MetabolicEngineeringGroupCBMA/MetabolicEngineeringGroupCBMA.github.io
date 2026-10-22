---
publish: true
---

The levels of reproducibility:

🔬 The Experimental Scale (From Easiest to Hardest)

- **Repeatability:** You do the test again in your own lab and get the same result.
- **Reproducibility:** Someone else uses **your data and code** and gets the same result.
- **Replicability:** Someone else collects **new data** using your methods and gets a similar result.
- **Generalizability:** The result holds true even in a completely different setting or group of people.

💻 The Software & Code Scale (From Worst to Best)

- **Level 0 (Unreliable):** It only works on your computer today. If you restart it, it might break.
- **Level 1 (Manual):** It works for others, but they have to manually install tools and follow a list of instructions.
- **Level 2 (Automated):** The code automatically downloads the exact package versions it needs to run.
- ==Level 2<3== 🎯 This is good enough for bioinformatics IMHO.
- **Level 3 (Locked Environment):** The project is packaged in a virtual "container" (like [Docker](https://www.docker.com/resources/what-container/#:~:text=A%20container%20is%20a%20standard%20unit%20of%20software%20that%20packages%20up%20code%20and%20all%20its%20dependencies%20so%20the%20application%20runs%20quickly%20and%20reliably%20from%20one%20computing%20environment%20to%20another.) or a VM) that freezes the entire system, ensuring it runs identically anywhere.
- **Level 4 (Declarative Build):** The environment is defined by a declarative specification with every input (compiler, libraries, system packages) pinned by cryptographic hash, so rebuilding it from source gives the same result at any time and place (e.g., **Nix**, **GNU Guix**).

| Feature                  | Docker Container                       | Virtual Machine (VM)                 |
| ------------------------ | -------------------------------------- | ------------------------------------ |
| **Virtualization Layer** | App/OS layer (Software)                | Hardware layer                       |
| **Operating System**     | Shares the **host OS kernel**          | Runs its own full **guest OS**       |
| **Size**                 | Very lightweight (typically Megabytes) | Heavyweight (typically Gigabytes)    |
| **Startup Time**         | Seconds or milliseconds                | Minutes (needs to boot an entire OS) |
| **Managed By**           | Docker Engine                          | Hypervisor (e.g., ESXi, VirtualBox)  |

---

Where to get packages? Depends on

- Conda packages:
  - conda-forge <https://conda-forge.org/packages>
  - Bioconda <https://bioconda.github.io/conda-package_index.html>
- Pypi <https://pypi.org>
  - Python wheels (.whl) = pre-built binary distribution
  - Source Distributions / sdists (.tar.gz) = archive containing the raw source code along with metadata (`PKG-INFO`).

---

How to specify a Python environment?

`requirements.txt`

```yaml
# requirements.txt 
# This is a comment, #-prefixed lines are ignored. It is possible to specify requirements as plain package names:
pytest
pytest-cov
beautifulsoup4

# The syntax supported here is the same as that of requirement specifiers.
docopt == 0.6.1
requests [security] >= 2.8.1, == 2.8.* ; python_version < "2.7"
urllib3 @ https://github.com/urllib3/urllib3/archive/refs/tags/1.26.8.zip

# It is possible to refer to other requirement files or constraints files.
-r other-requirements.txt
-c constraints.txt

# It is possible to refer to URLs.
http://wxpython.org/Phoenix/snapshot-builds/wxPython_Phoenix-3.0.3.dev1820+49a8884-cp34-none-win_amd64.whl
```

Conda uses `environment.yml`:

```yaml
# environment.yml
name: myenv
channels:
  - conda-forge
dependencies:
  - python
  - numpy
```

Conda can install R and almost any other language.

**Option A: build the environment, then export**

```bash
conda create -n myproj -c conda-forge -c bioconda python=3.11 samtools=1.20
conda activate myproj
conda install -c bioconda bcftools=1.20     # add more as needed

conda env export --from-history > environment.yaml
```

`--from-history` lists only the packages you explicitly requested, with the version constraints you typed. This makes the file portable across platforms, but only as tightly pinned as your requests were. It also omits pip-installed packages, so add those by hand.

Plain `conda env export` writes every package with exact version and build string. That is fully pinned but platform-specific, so it often **fails** on another OS.

`conda env export --no-builds` is a middle ground: exact versions, no build strings.

**Option B: write the file by hand (my preference for a project)**

```yaml
name: myproj
channels:
  - conda-forge
  - bioconda
dependencies:
  - python=3.11
  - samtools=1.20
  - bcftools=1.20
  - pip
  - pip:
      - some-pip-only-package==0.4.2
```

Then create and update it with:

```bash
conda env create -f environment.yaml
```

**Getting to a real Level 2:** a hand-edited or `--from-history` file is only as pinned as you make it. To get exact, hash-verified resolution across platforms, generate a lockfile from it:

```bash
conda-lock lock -f environment.yaml -p linux-64 -p osx-arm64
conda-lock install -n myproj conda-lock.yml
```

**Pixi** uses the conda ecosystem (conda-forge, bioconda)

```bash
pixi init
pixi add python=3.11 samtools bcftools
pixi add --pypi some-pip-only-package
```

This edits the file `pixi.toml` and writes a `pixi.lock` automatically, so the lockfile is produced as part of normal use rather than as an extra step. If you want a uv-like experience with bioconda packages, pixi is the tool to look at.
