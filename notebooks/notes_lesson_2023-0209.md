
`#notes_lesson_2023-0209.md`

<details>
<summary><font size="+2"><b><i>Table of Contents</i></b></font></summary>
<!-- MarkdownTOC -->

1. [Message](#message)
1. [Things we talked about](#things-we-talked-about)
	1. [The `declare` and `typeset` commands](#the-declare-and-typeset-commands)
		1. [*More details \(not a priority; save for future use\)*](#more-details-not-a-priority-save-for-future-use)
		1. [*Examples: The `declare` and `typeset` commands*](#examples-the-declare-and-typeset-commands)
	1. [`for` loops&mdash;and some info on variables and arrays](#for-loopsmdashand-some-info-on-variables-and-arrays)
		1. [*Examples: `for` loops&mdash;and some info on arrays*](#examples-for-loopsmdashand-some-info-on-arrays)
	1. [When writing code, it is considered good practice to break lines at 80 characters](#when-writing-code-it-is-considered-good-practice-to-break-lines-at-80-characters)
		1. [*More details*](#more-details)
		1. [*Examples*](#examples)
	1. [Compute clusters and head and compute nodes](#compute-clusters-and-head-and-compute-nodes)
		1. [*More details*](#more-details-1)
		1. [*Examples*](#examples-1)
	1. [Cluster management programs such as `SLURM`, `grid`, and `LSF`](#cluster-management-programs-such-as-slurm-grid-and-lsf)
		1. [*More details*](#more-details-2)
		1. [*Examples*](#examples-2)
	1. [Logging into a head node \(`rhino01`, `rhino02`, `rhino03`\) at FHCC](#logging-into-a-head-node-rhino01-rhino02-rhino03-at-fhcc)
		1. [*More details*](#more-details-3)
		1. [*Examples*](#examples-3)
	1. [The `grabnode` command for interactive work on the FHCC cluster](#the-grabnode-command-for-interactive-work-on-the-fhcc-cluster)
		1. [*More details*](#more-details-4)
		1. [*Examples*](#examples-4)
	1. [The `sbatch` and `srun` commands for non-interactive commands on the FHCC cluster](#the-sbatch-and-srun-commands-for-non-interactive-commands-on-the-fhcc-cluster)
		1. [*More details*](#more-details-5)
		1. [*Examples*](#examples-5)
	1. [Threads/cores/CPUs](#threadscorescpus)
		1. [*More details*](#more-details-6)
		1. [*Examples*](#examples-6)
	1. [GNU versus BSD utility programs](#gnu-versus-bsd-utility-programs)
		1. [*More details*](#more-details-7)
		1. [*Examples*](#examples-7)
	1. [Programs that are used to download others programs](#programs-that-are-used-to-download-others-programs)
		1. [*More details*](#more-details-8)
		1. [*Examples*](#examples-8)
	1. [Downloading NGS files by searching for them in public databases](#downloading-ngs-files-by-searching-for-them-in-public-databases)
		1. [*More details*](#more-details-9)
		1. [*Examples*](#examples-9)
	1. [Downloading files with the `wget` and `curl` commands](#downloading-files-with-the-wget-and-curl-commands)
		1. [*More details*](#more-details-10)
		1. [*Examples*](#examples-10)

<!-- /MarkdownTOC -->
</details>
<br />

<a id="message"></a>
## Message
<details>
<summary><i>Click to view message</i></summary>

Hi Rina and Rachel,

I am putting together a list of everything we talked about in the course of our lesson last week. I am organizing and adding details to that list, and all of that in-progress work is [here]. Please look it over these things and let me know if you have any questions.

Did we decide on a time to meet next? I don't recall that we did. If it's OK for you, let's skip the formal meeting this week. Instead, let's meet informally if you have any questions or want to talk about coding/analysis-related things. Feel free to come and talk with me anytime.

For the following week, when would you like to meet? Sometime on Thursday or Friday works for me.

Also, you have been working through the lessons in Parts 1 and 2 [here](https://github.com/hbctraining/Intro-to-shell-flipped/blob/master/schedule/links-to-lessons.md). Can you let me know where you are in this or if you have completed all the lessons for Parts 1 and 2?

Our next step is to begin [ChIP-seq work](https://github.com/hbctraining/Intro-to-ChIPseq-flipped/blob/main/schedule/README.md). Please look over these materials for basic information on ChIP-seq (and ChIP-seq-like experiments such as ATAC-seq, MNase-seq, and CUT&RUN):
- [slide deck 1](https://github.com/hbctraining/Intro-to-ChIPseq-flipped/blob/main/lectures/Introduction_to_ChIP-seq_2022.pdf)
- [slide deck 2](https://physiology.med.cornell.edu/faculty/skrabanek/lab/angsd/lecture_notes/13_lecture.pdf)

Meanwhile, I will adapt [these materials](https://github.com/hbctraining/Intro-to-ChIPseq-flipped/blob/main/schedule/README.md) for use with your ChIP-seq datasets of interest (what we downloaded last time we met); I will also adapt Christine's analysis scripts for our use.

Thanks,  
Kris
</details>
<br />
<br />

<a id="things-we-talked-about"></a>
## Things we talked about
<a id="the-declare-and-typeset-commands"></a>
##### <u>The `declare` and `typeset` commands</u>
+ In `bash` (and `zsh`), a variable is created by assigning a value to its reference. Although the built-in `declare` statement does not need to be used to explicitly declare a variable in `bash`, the command is often used for more advanced tasks involving variables.
+ Although `bash` variables don't need to be explicitly declared, variables in some other programming languages do; these languages include `Java`, `C`, and `C++`. Note that variables ___do not___ need to be explicitly declared in `R` or `Python`, two other languages we will use in our work.
+ In our lesson, we discussed the use of `declare -p`, `declare -a`, and `declare -A`
	* `declare -p`: Display options and attributes of variables.
	* `declare -a`: The variable is an indexed array.
	* `declare -A`: The variable is an associative array.
+ `declare` and `typeset` are the same commands ([what-is-the-difference-between-declare-and-typeset](https://unix.stackexchange.com/questions/66007/what-is-the-difference-between-declare-and-typeset))

<a id="more-details-not-a-priority-save-for-future-use"></a>
###### *More details (not a priority; save for future use)*
<details>
<summary><i>Click to view links</i></summary>

- [linuxhint.com/bash_declare_command/](https://linuxhint.com/bash_declare_command/)
- [phoenixnap.com/kb/bash-declare](https://phoenixnap.com/kb/bash-declare)
- [tldp.org/LDP/abs/html/declareref.html](https://tldp.org/LDP/abs/html/declareref.html)
</details>
<br />

<a id="examples-the-declare-and-typeset-commands"></a>
###### *Examples: The `declare` and `typeset` commands*
<details>
<summary><i>Click to view code</i></summary>

```bash
#!/bin/bash

#  Example 1: declare -p ------------------------------------------------------
test="chicken"  # same as `declare test="chicken"`
declare -p test
# declare -- test="chicken"


#  Example 2: declare -a ------------------------------------------------------
declare -a numbers
numbers=(1 2 3 4 5)
for i in "${numbers[@]}"; do
	echo "${i}"
done
# 1
# 2
# 3
# 4
# 5


#  Example 3: delcare -A ------------------------------------------------------
declare -A numbers_names
numbers_names["zero"]="Kris"
numbers_names["one"]="Rina"
numbers_names["two"]="Rachel"
for i in "${!numbers_names[@]}"; do
	echo "  Key: ${i}"
	echo "Value: ${numbers_names[${i}]}"
	echo ""
done
#   Key: two
# Value: Rachel
#
#   Key: one
# Value: Rina
#
#   Key: zero
# Value: Kris
```
</details>
<br />

<a id="for-loopsmdashand-some-info-on-variables-and-arrays"></a>
##### <u>`for` loops&mdash;and some info on variables and arrays</u>
+ A `for` loop is a programming language statement that allows code to be executed repeatedly&mdash;it is the repetition of a process at the shell prompt or within a shell script.
+ It is common over elements in arrays (an 'element' is each value in an array), and this is what we did in *Example 2* and *Example 3* [above](#examples-the-declare-and-typeset-commands)
	* To access the individual elements in an array, you have to use a special syntax: `"${numbers[0]}"`, `"${numbers[1]}"`
		- Note that the dollar sign (`$`) quotes (`""`), pointy brackets (`{}`), and square brackets (`[]`) are all important here
		- The dollar sign (`$`) is how we access variable/array contents in `bash` and `zsh` (see example code below)
	* Also, remember that `bash` is a <u>0-based</u> programming language (the first index is `0`); `zsh`, on the other hand, is a <u>1-based</u> programming language (the first index is `1`)
		- ___Keep this in mind when writing and testing code on your Mac, which has `zsh` installed as the default shell!___

<a id="examples-for-loopsmdashand-some-info-on-arrays"></a>
###### *Examples: `for` loops&mdash;and some info on arrays*
<details>
<summary><i>Click to view code</i></summary>

```bash
#!/bin/bash

#  Example 1: `echo` with and without a dollar symbol ($) ---------------------
test="turkey"
echo test
# test
echo $test
# turkey


#  Example 2: `for`` loops ----------------------------------------------------
for i in 6 7 8 9 10; do
	echo "${i}"
done
# 6
# 7
# 8
# 9
# 10

numbers_2=(6 7 8 9 10)
for i in "${numbers_2[@]}"; do
	echo "${i}"
done
# 6
# 7
# 8
# 9
# 10


#  Example 3: Using a `for`` loop to download fastqs from the ENA -------------
#!/bin/bash

#  Files from this project: ebi.ac.uk/ena/browser/view/PRJNA279130
#+ 
#+ These are Jeff's Rpd3 ChIP-seq data
files=(
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/005/SRR1924325
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/006/SRR1924326
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/007/SRR1924327
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/008/SRR1924328
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/009/SRR1924329
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/000/SRR1924330
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/001/SRR1924331
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/002/SRR1924332
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/003/SRR1924333
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/004/SRR1924334
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/005/SRR1924335
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/006/SRR1924336
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/007/SRR1924337
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/008/SRR1924338
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/009/SRR1924339
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/000/SRR1924340
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/001/SRR1924341
    ftp.sra.ebi.ac.uk/vol1/srr/SRR192/002/SRR1924342
)

#  Test the contents of the array
for i in "${files[@]}"; do
	echo "${i}"
done

#  Download all the files in the array
for i in "${files[@]}"; do
    echo "Downloading ${i}"
    curl "${i}" > "$(basename "${i}")"
done
```
</details>
<br />

<a id="when-writing-code-it-is-considered-good-practice-to-break-lines-at-80-characters"></a>
##### <u>When writing code, it is considered good practice to break lines at 80 characters</u>
<a id="more-details"></a>
###### *More details*
<a id="examples"></a>
###### *Examples*

<a id="compute-clusters-and-head-and-compute-nodes"></a>
##### <u>Compute clusters and head and compute nodes</u>
<a id="more-details-1"></a>
###### *More details*
<a id="examples-1"></a>
###### *Examples*

<a id="cluster-management-programs-such-as-slurm-grid-and-lsf"></a>
##### <u>Cluster management programs such as `SLURM`, `grid`, and `LSF`</u>
- What they are and what they do
- FHCC uses `SLURM`

<a id="more-details-2"></a>
###### *More details*
<a id="examples-2"></a>
###### *Examples*

<a id="logging-into-a-head-node-rhino01-rhino02-rhino03-at-fhcc"></a>
##### <u>Logging into a head node (`rhino01`, `rhino02`, `rhino03`) at FHCC</u>
<a id="more-details-3"></a>
###### *More details*
<a id="examples-3"></a>
###### *Examples*

<a id="the-grabnode-command-for-interactive-work-on-the-fhcc-cluster"></a>
##### <u>The `grabnode` command for interactive work on the FHCC cluster</u>
<a id="more-details-4"></a>
###### *More details*
<a id="examples-4"></a>
###### *Examples*

<a id="the-sbatch-and-srun-commands-for-non-interactive-commands-on-the-fhcc-cluster"></a>
##### <u>The `sbatch` and `srun` commands for non-interactive commands on the FHCC cluster</u>
<a id="more-details-5"></a>
###### *More details*
<a id="examples-5"></a>
###### *Examples*

<a id="threadscorescpus"></a>
##### <u>Threads/cores/CPUs</u>
<a id="more-details-6"></a>
###### *More details*
<a id="examples-6"></a>
###### *Examples*

<a id="gnu-versus-bsd-utility-programs"></a>
##### <u>GNU versus BSD utility programs</u>
<a id="more-details-7"></a>
###### *More details*
<a id="examples-7"></a>
###### *Examples*

<a id="programs-that-are-used-to-download-others-programs"></a>
##### <u>Programs that are used to download others programs</u>
- e.g., `brew`, `conda`/`mamba`, `GitHub`, `apt-get`, `pip3`, etc.

<a id="more-details-8"></a>
###### *More details*
<a id="examples-8"></a>
###### *Examples*

<a id="downloading-ngs-files-by-searching-for-them-in-public-databases"></a>
##### <u>Downloading NGS files by searching for them in public databases</u>
- [NCBI](https://www.ncbi.nlm.nih.gov/)
	+ [SRA](https://www.ncbi.nlm.nih.gov/sra)
	+ [GEO](https://www.ncbi.nlm.nih.gov/geo/)
- [EBI](https://www.ebi.ac.uk/)
	+ [ENA](https://www.ebi.ac.uk/ena/browser/)
	+ [Biostudies](https://www.ebi.ac.uk/biostudies/) (formerly ArrayExpress)

(Also discussed using the "column" feature of ENA to download a tsv file, which is&mdash;for example&mdash;parsed and looped over to download files using their ftp entries)

<a id="more-details-9"></a>
###### *More details*
<a id="examples-9"></a>
###### *Examples*

<a id="downloading-files-with-the-wget-and-curl-commands"></a>
##### <u>Downloading files with the `wget` and `curl` commands</u>
<a id="more-details-10"></a>
###### *More details*
<a id="examples-10"></a>
###### *Examples*
