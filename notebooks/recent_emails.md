
`#recent_emails.md`
<br />

## ChIP-seq data
From: Hirano, Rina <rhirano@fredhutch.org>  
Sent: Thursday, February 9, 2023 11:11 AM  
To: Alavattam, Kris <kalavatt@fredhutch.org>  
Subject: ChIP-seq data

Hi Kris,
 
These are data that I want to analyze.
 
1, Brn1p (condensin), G1 ChIP
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM305999
 
2, Brn1p (condensin), G2/M ChIP
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM306011
 
3, Brn1p (condensin), Q, ChIP
https://www.ncbi.nlm.nih.gov/sra/SRX4092953[accn]
(input https://www.ncbi.nlm.nih.gov/sra/SRX4092954[accn])
 
I’m looking forward to analyzing them!

Rina Hirano  
Postdoctoral Research Fellow  
rhirano@fredhutch.org  
Tsukiyama Lab  
Basic Sciences Division  
Fred Hutch Cancer Research Center
<br />
<br />

## Bioinformatics lesson/meeting for tomorrow, Jan. 20
##### 1
From: Alavattam, Kris <kalavatt@fredhutch.org>  
Sent: Friday, February 3, 2023 2:06 PM  
To: Dell, Rachel H <rdell@fredhutch.org>; Hirano, Rina <rhirano@fredhutch.org>  
Subject: Re: Bioinformatics lesson/meeting for tomorrow, Jan. 20

(Put this after the call to .zfunctions)

```bash
# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/Users/kalavattam/miniconda3/bin/conda' 'shell.zsh' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/Users/kalavattam/miniconda3/etc/profile.d/conda.sh" ]; then
        . "/Users/kalavattam/miniconda3/etc/profile.d/conda.sh"
    else
        export PATH="/Users/kalavattam/miniconda3/bin:$PATH"
    fi
fi
unset __conda_setup

if [ -f "/Users/kalavattam/miniconda3/etc/profile.d/mamba.sh" ]; then
    . "/Users/kalavattam/miniconda3/etc/profile.d/mamba.sh"
fi
# <<< conda initialize <<<
```

##### 2
From: Alavattam, Kris <kalavatt@fredhutch.org>  
Sent: Friday, February 3, 2023 1:51 PM  
To: Dell, Rachel H <rdell@fredhutch.org>; Hirano, Rina <rhirano@fredhutch.org>  
Subject: Re: Bioinformatics lesson/meeting for tomorrow, Jan. 20

```bash
# Add zsh aliases.
if [[ -f ~/.zaliases ]]; then
    source ~/.zaliases
fi

# Add zsh functions.
if [[ -f ~/.zfunctions ]]; then
    source ~/.zfunctions
fi
```

##### 3
From: Alavattam, Kris <kalavatt@fredhutch.org>  
Sent: Friday, February 3, 2023 1:43 PM  
To: Dell, Rachel H <rdell@fredhutch.org>; Hirano, Rina <rhirano@fredhutch.org>  
Subject: Re: Bioinformatics lesson/meeting for tomorrow, Jan. 20

```bash 
# github.com/fabiomaia/linuxify
. ~/.linuxify
```

##### 4
From: Alavattam, Kris <kalavatt@fredhutch.org>  
Sent: Friday, February 3, 2023 8:35 AM  
To: Dell, Rachel H <rdell@fredhutch.org>; Hirano, Rina <rhirano@fredhutch.org>  
Cc: Tsukiyama, Toshio <ttsukiya@fredhutch.org>  
Subject: Re: Bioinformatics lesson/meeting for tomorrow, Jan. 20
 
Hi Rachel and Rina,
 
Today, when we meet, let’s review material in the two lessons I linked to [here](https://github.com/hbctraining/Intro-to-shell-flipped/blob/master/schedule/links-to-lessons.md) (Part 1 lessons 3 and 4), and let’s also continue to set up your systems following the info that I typed up [here](https://gist.github.com/kalavattam/7c49a6b0be8174cd565b6d607d9e2293) (Oh My Zsh, Linuxify, Powerline, etc.) and [here](https://gist.github.com/kalavattam/ffb14d6f096b674582d7c70d6af2b1f9) (conda/mamba). This will make your analyses easier to manage and perform, and ensure compatibility between your Macs and the FHCC cluster.
 
Thanks,  
Kris

##### 5
From: Alavattam, Kris <kalavatt@fredhutch.org>  
Date: Thursday, January 26, 2023 at 6:44 PM  
To: Dell, Rachel H <rdell@fredhutch.org>, Hirano, Rina <rhirano@fredhutch.org>  
Cc: Tsukiyama, Toshio <ttsukiya@fredhutch.org>  
Subject: Re: Bioinformatics lesson/meeting for tomorrow, Jan. 20

Hi Rachel and Rina,
 
Just as a reminder, we decided to move forward with Part 1 lessons 3 and 4 [here](https://github.com/hbctraining/Intro-to-shell-flipped/blob/master/schedule/links-to-lessons.md) (and if you have time, then try lesson 5 too). We also decided to meet next Friday, Feb. 3, at 1:00 p.m. Please feel free to ask me any questions or meet with me informally between now and then too. Rachel: I’ll take care of those points you raised.
 
Thanks,  
Kris

##### 6
From: Alavattam, Kris <kalavatt@fredhutch.org>  
Date: Thursday, January 26, 2023 at 1:53 PM  
To: Dell, Rachel H <rdell@fredhutch.org>, Hirano, Rina <rhirano@fredhutch.org>  
Cc: Tsukiyama, Toshio <ttsukiya@fredhutch.org>  
Subject: Re: Bioinformatics lesson/meeting for tomorrow, Jan. 20

https://github.com/hbctraining/Intro-to-shell-flipped/blob/master/schedule/links-to-lessons.md

##### 7
From: Alavattam, Kris  
Sent: Thursday, January 19, 2023 11:17 AM  
To: Dell, Rachel H <rdell@fredhutch.org>; Hirano, Rina <rhirano@fredhutch.org>  
Cc: Tsukiyama, Toshio <ttsukiya@fredhutch.org>  
Subject: Bioinformatics lesson/meeting for tomorrow, Jan. 20
 
Hi Rina and Rachel,  
cc Toshi
 
I want to get you both started with ChIP-seq data as soon as possible. But before that, we need to make sure you’re comfortable with using Shell/the command line. From there, we can start doing ChIP-seq-related analyses using Shell and various command line tools, and then we can move on to learning and doing work in R/RStudio.
 
If you have time, please look over [slides 1–17](https://hbctraining.github.io/Intro-to-shell-flipped/lectures/Intro_to_workshop.pdf) here before we meet tomorrow.
 
Tomorrow, let’s start working through [this lesson](https://hbctraining.github.io/Intro-to-shell-flipped/lessons/01_the_filesystem.html#copying-example-data-folder) together (you can ignore the material before this header). After that, we can work through [this lesson](https://hbctraining.github.io/Intro-to-shell-flipped/lessons/02_wildcards_shortcuts.html). Please download the attached data, which we’ll need to work through these lessons. We’ll discuss next steps from there.
 
The big picture:
First, we’ll work through some of the basic Shell material here: https://hbctraining.github.io/Intro-to-shell-flipped/schedule/
Then, we’ll shift focus to direct ChIP-seq work here: https://github.com/hbctraining/Intro-to-ChIPseq-flipped/blob/main/schedule/README.md
Then, when we’re part of the way through the above, we’ll start working on R-related things, including more ChIP-seq work: https://github.com/hbctraining/Intro-to-R-flipped/blob/master/schedules/links-to-lessons.md
 
Let’s also discuss ways you can spend a little bit of time each day practicing and studying, which will be important to becoming confident with these analyses.
 
Thanks,  
Kris
