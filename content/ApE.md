---
publish: true
---

ApE (A Plasmid Editor) is a freely available DNA Manipulation and visualization program. I works on macOS and Windows as well as on Linux.

It is not necessary to install ApE to use it, you can use it from a folder on your desktop.

Go [here](https://jorgensen.biology.utah.edu/wayned/ape) to get ApE, click on the link for your OS as indicated below.

[![[ape_download.png]]](https://jorgensen.biology.utah.edu/wayned/ape)

## Introduction to ApE

[![[ApE-20240924104257314.png]]](https://youtu.be/HTq91gJDSqk?si=5oT0bDhj6QIf4JwW)

[![[ApE-20240924104312073.png]]](https://youtu.be/vDSiM2M_6JU?si=lpYg1SiVIt0a-mfq)

[![[Pasted image 20240924104322.png]]](https://youtu.be/8n5yzd7hlXA?si=Aaoo4kIVvLdYnJX9)

### How to linearize a circular sequence at a specific location.

1. Locate the cursor at the desired location where you want to cut the vector. Make sure sequence is circular.

![[ApE_locate_linearization_site.png]]

1. Select ApE Edit>"Linearize @ insert site" (see below).

![[ApE_linearize_insertion_site.png]]

The sequence is now linear beginning at the location of the cursor.

![[ApE_linearized_sequence.png]]

### More info

[![[ApE-20240924103839571.png|496]]](https://youtu.be/zYqN9pF3ZVs)

<https://github.com/gear-genomics/wily-dna-editor>

[Annotate the PTC sequence with ApE](http://bio305lab.wikidot.com/exercise2012:exercise-1)

<https://wiki.tcl-lang.org/page/sha1>

def SmallestRotation(s):
"""Find the rotation of s that is smallest in lexicographic order.
Algorithm according to Duval 1983:
Pierre Duval, Jean. 1983. “Factorizing Words over an Ordered Alphabet.”
Journal of Algorithms & Computational Technology\* 4 (4) (December 1):
363–381.
Algorithms on strings and sequences based on Lyndon words.
David Eppstein, October 2011.
<https://gist.github.com/dvberkel/1950267>
"""
prev, rep = None, 0
ds = 2 \* s
lens = len(s)
lends = len(ds)
old = 0
k = 0
w = ""
while k < lends:
i, j = k, k + 1
while j < lends and ds\[i] <= ds\[j]:
i = (ds\[i] == ds\[j]) and i + 1 or k
j += 1
while k < i + 1:
k += j - i
prev = w
w = ds\[old:k]
old = k
if w == prev:
rep += 1
else:
prev, rep = w, 1
if len(w) \* rep == lens:
return w \* rep

<https://openwetware.org/wiki/Software>

# changed here!

# append result "\[format "LOCUS       %-16s %+11s bp %-3s%-6s     %-8s %-3s %-11s" $genbank_locus_name [string length $text] $stranded $genbank\_type $info($w,circular) \$genbank\_division\_code \[string toupper \[clock format \[clock seconds] -format "%d-%h-%Y"]]]\n"

append result "\[format "LOCUS       %-16s %+11s bp %-3s%-6s  %-8s %-3s %-11s" $genbank_locus_name [string length $text] $stranded $genbank\_type $info($w,circular) \$genbank\_division\_code \[string toupper \[clock format \[clock seconds] -format "%d-%h-%Y"]]]\n"

Also
6\. ABI [[files]] can be linked into sequence [[files]] by dragging the link icon from
the ABI window onto a sequence window. When the sequence window is saved, the
data from the abi file is saved with it in a text-encoded format so that the
file can still be opened with a text editor.

### space in filename

parse \$argv into filenames even if these are spaces
or
tell gnome-open that every filename should be enclosed by ""

> a
> aaa
> c
> ccc

### cut paste

line 3857
[AppMain.tcl](file:/home/bjorn/.ApE/AppMain.tcl)

<http://tech.groups.yahoo.com/group/wikidPad/message/4527>
<<
PRIMARY selection doesn't exist or form "STRING" not defined
PRIMARY selection doesn't exist or form "STRING" not defined gggatcc
while executing
"selection get -displayof $w -selection PRIMARY"
   (procedure "clip_paste" line 7)
   invoked from within
"clip_paste $w"
(procedure "keyevent\_manager" line 113)
invoked from within
"keyevent\_manager .dna\_window1 Control v "
(command bound to event)

> >

########### Sunday, June 07 2009

## paste  function

###########

proc clip\_paste {w {direction normal}} {
global info
global tcl\_platform

# tk\_messageBox -message "clip paste"

if {(\$tcl\_platform(platform) == "unix") && (\[tk windowingsystem] != "aqua")} {

sputs paste:CLIPBOARD:\[selection get -displayof \$w -selection CLIPBOARD]

# sputs paste:PRIMARY:\[selection get -displayof \$w -selection PRIMARY]

# if {\[catch {set text \[selection get -displayof \$w -selection PRIMARY]}] != 0} {return}

```
# }  ###
# else  ###
# {                                                                                       ###
if {[catch { set text [selection get -displayof $w -selection CLIPBOARD]}] != 0} {return}
```

# }
