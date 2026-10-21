---
publish: true
---

# The Unix philosophy and BASH scripting

## The shell and the Unix philosophy

Unix is a multi-user, and multitasking computer operating system created in 1969 at Bell Labs. It forms the genetic and philosophical foundation for modern computing, influencing how files, permissions, and command-line tools work across almost all contemporary operating systems.

Linux is a free, open-source Unix-like operating system. While it was built from scratch and does not contain original Unix code, it mimics Unix design, commands, and file structures.

The Unix philosophy is a minimalist approach to software design created by pioneers like Ken Thompson, Dennis Ritchie, and Doug McIlroy at Bell Labs.

Core Principles:

- **Do One Thing Well:** Build focused tools rather than bloated, all-in-one applications.
- **Work Together:** Design programs so the output of one can feed directly into another via pipelines.
- **Universal Text Streams:** Use plain text as a common interface so components can easily parse and exchange data.
- **Clarity Over Cleverness:** Write code that is easy for humans to read, maintain, and debug.
- **Silence is Golden:** Programs should print output only when something unusual or important happens.
- **Programmer Time Over Machine Time:** Optimize for human efficiency and reuse rather than squeezing out every microsecond of raw hardware speed.

[Basics of the Unix Philosophy - Harvard](https://cscie2x.dce.harvard.edu/hw/ch01s06.html)

A terminal provides an interface to a shell. An operating system shell is named a "shell" because it forms the outermost layer surrounding the core of the operating system (the kernel). The Bourne Again SHell == BASH is a popular shell.

Bash is also an interpreter that can execute code in a similar way to R an Python.

Use Bash on Linux, macOS or through Git Bash/WSL+Ubuntu on Windows
![[Mestrado em Biologia Computacional Molecular e Ambiental/BASHp0qpiu.png]]

Command shell and PowerShell looks similar but use different syntax.

- [PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/overview)
- [Windows Command Shell](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cmd)
- [bash](https://www.gnu.org/software/bash/) - popular on Linux
- [zsh](https://support.apple.com/102360) - popular on macOS

---

## Download a file from the shell

### Go to desktop from anywhere

```bash

cd /mnt/c/USERS/<username>/Desktop # Works on WSL+Ubuntu, this will take you to the "Windows" Desktop

cd %USERPROFILE%/Desktop  # Works on Anaconda Prompt, goes to the windows desktop.

cd ~/Desktop  # Works on PowerShell, Not on Anaconda Prompt, on WSL+Ubuntu no such folder.
```

```bash
wget https://raw.githubusercontent.com/biopython/biopython/master/Doc/examples/ls_orchid.fasta
```

wget is not available on the Anaconda Prompt, use curl:

```bash
curl -L -O "https://raw.githubusercontent.com/biopython/biopython/master/Doc/examples/ls_orchid.fasta"
```

---

## Commands that can be used to rapidly inspect a text file

```bash
ls -lh ls_orchid.fasta        # Show the file and its size
head ls_orchid.fasta          # Inspect the beginning
less ls_orchid.fasta          # Browse; press q to quit
wc -l ls_orchid.fasta         # Count lines instead
```

---

## Navigate and organize files

```bash
pwd  # Show the current directory
ls  # List files
cd  # Change directory
mkdir results  # Create a directory
cp ls_orchid.fasta results/ls_orchidy.fasta  # Copy a file to a subdirectory
mv old.fasta new.fasta  # Move or rename a file
rm results/ls_orchidy.fasta  # Remove a file
```

Paths:

```bash
18:10 $ cd /  # filesystem root on linux
✔ / 
18:10 $ ls 
bin boot dev home  ...
✔ / 
18:10 $ cd ~   # tilde is your home directory
✔ ~ 
18:11 $ ls 
bin         Dropbox                             learning.mp3  Obsidian.AppImage                 Teaching
brown.opus  FatVal                              micromamba    Pictures                          Templates
Desktop
✔ ~ 
18:11 $ ls .  # . is the current directory 
bin         Dropbox                             learning.mp3  Obsidian.AppImage                 Teaching
brown.opus  FatVal                              micromamba    Pictures                          Templates
Desktop
✔ ~ 
18:11 $ cd Desktop/
✔ ~/Desktop 
18:12 $ ls
 agregação                                            'Mariana Santos'
 bash-script.sh~                                      'Mestrado em Biologia Computacional Molecular e Ambiental'
'Bruna Oliveria'                                       mestradoembioqumicaaplicadadatasexamesderecurso
'Catarina Martins'                                    'MetabolicEngineeringGroupCBMA GitHub Org'
 DABDGE                                                misc
 dig                                                  'ole1 deletion primer design'
 ERASMUS26                                             ongoing-work
 euproject                                             pHEY-1
'file processing'                                     'primer screen'
 garmin                                               'pTA1 sequence'
 gel                                                   pTA5_FASIIe
 genética--manual-pl--mutagénese-24-25-corrigido.doc   pVG1.gbk
 humb                                                  pydna
 icebox.jpeg                                           python_packages
 ideas                                                 river2ocean
'Link to mec GitHub Org'                              'sequences with IS1 transposons'
'Link to Teaching'                                     strains
'Luana Moura'                                          work
✔ ~/Desktop 
18:12 $ cd ..  #  .. is the parent directory, use this to go "up". 
✔ ~ 
18:12 $ ls
bin         Dropbox                             learning.mp3  Obsidian.AppImage                 Teaching
brown.opus  FatVal                              micromamba    Pictures                          Templates
Desktop
```

---

## Get help and work efficiently

- `command --help` and `man command`: options and documentation; support varies by command and installation.
- Tab: complete paths and command names.
- Up arrow or Ctrl+R: recall previous commands.
- Ctrl+C: interrupt a running command.
- `nano script.sh`: edit a text file; Ctrl+O saves, Enter confirms the filename, Ctrl+X exits.

---

## Globbing and searching with regexp (regular expression)

The shell expands filename patterns before running a command:

```bash
ls *.fasta
ls sample?.tsv
ls sample[12].tsv
```

`*` matches any string, `?` one character and `[12]` either `1` or `2`. A glob selects filenames; a regular expression searches text.

```bash
head "sample one.fasta"
grep '^>' ls_orchid.fasta  # returns the line of the match
grep -c '^>' ls_orchid.fasta  # Count sequence headers

```

`grep '^>'` selects FASTA header lines; `grep -c '^>'` counts them. Single quotes preserve literal text. Double quotes preserve spaces while allowing variable expansion, as in `"$sample"`.

## Streams, pipes and redirection

- **`stdin` (Standard Input / Stream 0):** The input data the program reads. By default, this is your keyboard.
- **`stdout` (Standard Output / Stream 1):** The normal output data the program produces. By default, this goes to your screen.
- **`stderr` (Standard Error / Stream 2):** Error messages produced by the program. By default, this also goes to your screen, but it is kept separate from `stdout` so errors don't mix with normal data

Programs can read **stdin**, write results to **stdout**, and write diagnostics to **stderr**.

The pipe (`|`) sends the standard output of `appA` to the standard input of `appB`

```bash
appA | appB
```

Redirection (`>`)

| Syntax                   | Purpose                                              |
| ------------------------ | ---------------------------------------------------- |
| `command > results.txt`  | Write stdout to a file, overwriting existing content |
| `command >> results.txt` | Append stdout to a file                              |
| `command 2> errors.log`  | Write stderr to a file                               |
| `command < input.txt`    | Read stdin from a file                               |

<!--
## Select columns, filter rows and summarize

For a headerless, tab-separated annotation file with one record per line and a category in column 3:

```bash
cut -f 3 annotations.tsv | sort | uniq -c | sort -nr > category_counts.txt
```

`cut` selects columns, `sort` groups identical values, `uniq -c` counts adjacent repetitions, and `sort -nr` orders counts from largest to smallest.

For a tab-separated GWAS table whose p-value is column 4:

```bash
awk -F '\t' 'NR == 1 || $4 < 5e-8' variants.tsv > significant.tsv
```

This retains the header and filters data rows numerically. Inspect the actual header and column order first; the example assumes valid numeric p-values without missing values.
-->

## Compressed biological data

- `gzip file.fastq`: compress a file; normally replaces the original.
- `gunzip file.fastq.gz`: decompress a file; normally replaces the compressed file.
- `zcat reads.fastq.gz | head -n 8`: inspect decompressed text without creating a full decompressed file. On some macOS installations, use `gzcat`.
- `tar -tzf dataset.tar.gz`: list archive members.
- `tar -xzf dataset.tar.gz`: extract the archive into the current directory.

## Variables, loops and reusable scripts

Count sequences:

```bash
sample="ls_orchid.fasta"
grep -c '^>' "$sample"
```

A loop repeats a command for each matching file in a directory:

```bash
for sample in *.fasta; do
    printf '%s\t' "$sample"
    grep -c '^>' "$sample"
done
```

Run this in a directory containing FASTA files. Quote `"$sample"` so spaces in filenames are preserved.

Save a reusable command in `count_sequences.sh`:

```bash
#!/usr/bin/env bash
# First argument: the input FASTA file.
grep -c '^>' "$1"
```

Run it with an input filename:

```bash
bash count_sequences.sh sequences.fasta
```

The first line is the **shebang**; `"$1"` is the first script argument.

## Exit status and conditional execution

- `$?`: exit status of the preceding command; zero conventionally means success.
- `appA && appB`: run `appB` only if `appA` succeeds.
- `appA || appB`: run `appB` only if `appA` fails.
- `grep` returns 1 when no lines match; this can be an expected result.
- A pipeline normally reports the last command's status. `set -o pipefail` makes failures in earlier stages visible in the pipeline status too.

## Practical sequence

1. Inspect a FASTA file and identify its record structure.
2. Count sequences from header lines rather than total lines.
3. Inspect a TSV file and identify its header and columns.
4. Filter rows, select columns and summarize categories with a pipeline.
5. Save the result in a separate file.
6. Turn the commands into a script and repeat across input files.

Important concepts not covered here: `sed`, advanced regular expressions, process substitution and job control.

<!--# BASH scripting / pipelines, The Unix philosophy

## Best matches for this class

### 1. BASH programming for biologists — genomics examples and guided lessons

**Wilkins, Owen M.; Campbell, Ross; Yosufzai, Zelaikha; Doe, Valena; Soucy, Shannon M. (2024).** *Cloud-based introduction to BASH programming for biologists*. Briefings in Bioinformatics, 25(Supplement 1), bbae244.

- [Paper / DOI](https://doi.org/10.1093/bib/bbae244)
- [Open in Zotero](zotero://select/library/items/7492Q9DA)
- [Local PDF](</home/bjorn/Zotero/storage/NGPWACAL/Wilkins et al. - 2024 - Cloud-based introduction to BASH programming for biologists.pdf>)
- Zotero item key: `7492Q9DA`; citation key: `wilkinsCloudbasedIntroductionBASH2024`.
- [NIGMS Sandbox repository cited in the paper](https://github.com/NIGMS/NIGMS-Sandbox). The paper was inspected through Recoll's indexed text; the current repository and notebooks have not been checked.

**Most useful sections:** submodule 1 introduces the terminal, paths and directories; submodule 3 uses FASTA, FASTQ and GFF files to introduce `grep` and pipes; submodule 4 introduces loops, scripts and the difference between `>` and `>>`. These sections are the strongest match for today's topic. Lessons include challenges with hints and answers.

Submodules 5–6 progress to software environments, FastQC/MultiQC, genome assembly and annotation. These provide context for why bioinformatics uses pipelines, but are more extensive than an introductory Bash session.

**Teaching suggestion:** adapt the file inspection and looping exercises for a local terminal. The published course uses Google Cloud and Jupyter notebooks, so its complete workflow requires preparation; it is not a verified ready-to-run local lesson.

### 2. EMBL-EBI introduction to BASH — a practical with GWAS results

[EMBL_EBI_GB_intro_bash_KC_questions](https://docs.google.com/document/d/15UlHfd7tV358JX6-oSUk_FbNrbK-6Gbsoi8tjzw4wfU/edit)

Confirmed in your accessible Google Drive and read in full. The sheet is headed **11 November 2025**, pre-course session, *Genome bioinformatics: from short- to long-read sequencing*.

It uses a subset of two million autosomal variants from a FinnGen cardiovascular-disease GWAS. The tasks are:

1. Write a script to extract `finngen_cvd_gwas.tar.gz` and decompress the chromosome files.
2. Combine the results into one text file, retaining exactly one header, and count variants.
3. Count variants separately for each chromosome.
4. Filter for p-values below `5 × 10⁻⁸` using `awk` and count the remaining variants.

**Why it fits:** a concrete biological reason to combine small command-line tools, use loops and pipes, and distinguish data rows from headers. The sheet says students do not need prior knowledge of GWAS.

**Preparation needed:** the instructions assume `/home/training/pre_course_session/bashintro` on the original training system. The Drive document contains questions, but no dataset download or solutions. No matching dataset surfaced in the Recoll search; this does not establish that it is absent. Obtain the teaching dataset or adapt the exercise to a small table before using it in class.

## Supporting material already available

- **Carey, Maureen A.; Papin, Jason A. (2018), *Ten simple rules for biologists learning to program*.** [Zotero](zotero://select/library/items/EIKZ25XR), [DOI](https://doi.org/10.1371/journal.pcbi.1005871). Citation key: `careyTenSimpleRules2018`. Recoll locates a comparison of programming languages, including Bash, its use for executing programs, and learning resources. Useful background reading for biologists; less direct than the two practical resources above.
- [[Mestrado em Biologia Computacional Molecular e Ambiental/Plano de aulas - Outubro 2026|Existing teaching plan]] already proposes paths and text-file inspection, pipes and redirection, running Python from Bash, and a Bash script that reruns the individual project. Reuse those learning outcomes; its original session placement differs from the current Day 4 schedule.
- [[Mestrado em Biologia Computacional Molecular e Ambiental/Git&Github|Git & GitHub lesson]] has Windows/Git Bash/WSL setup material to revisit before the practical.
- [Older vault-root BASH note](/home/bjorn/myvault/BASH.md) contains shell startup files, recursive globs, history search, `mv` and `cp`. It is a reference note rather than a biological pipeline lesson. Its content has been preserved.
- [[grep]] contains personal search-and-replace examples, mostly using `rrep`; it needs adaptation before use as a beginner `grep` lesson.
- [Automate the Boring Stuff with Python — existing teaching PDF](</home/bjorn/Teaching/MetabolicEngineeringCourse2023/_material/MetabolicEngineeringCourse2018/MetabolicEngineeringCourse2018_public/automatetheboringstuffwithpython.pdf>): Recoll finds a short discussion of the Unix philosophy in Chapter 15, printed page 356 (PDF page 380). Useful as a conceptual bridge from Python to composing tools; not bioinformatics-specific.

## Suggested selection for Day 4

Start with Wilkins submodules 1, 3 and 4 for biological file inspection, pipes and scripting. Use the EMBL-EBI GWAS exercise as the practical once its data are available. Finish by connecting the same approach to a script that reruns each student's Python project.

For the Unix philosophy discussion, ask students to identify the separate jobs in a pipeline: reading files, selecting rows, extracting columns and counting results. This is a suggested teaching framing, not an existing exercise recovered from your collections.

## Search scope

Zotero searches included Bash, Unix, shell, the Wilkins paper and *Bioinformatics Data Skills*; the latter returned no title match. Recoll searches covered Bash/bioinformatics, shell/bioinformatics, Unix philosophy, older teaching files and the FinnGen/EMBL exercise names. Drive searches used Bash, Unix, shell and bioinformatics. No dedicated Unix-philosophy teaching deck surfaced. Search coverage depends on indexing and access; these are selected findings, not an exhaustive inventory.-->
