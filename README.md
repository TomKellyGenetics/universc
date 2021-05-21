---
title: "UniverSC: Single-cell processing across technologies"
author: "S. Thomas Kelly^1†^, Kai Battenberg^1,2†^, Makoto Hayashi^2^, Aki Minoda^1^ <br> ^1^ RIKEN Center for Integrative Medical Sciences, Suehiro-cho-1-7-22, Tsurumi Ward, Yokohama <br> ^2^ RIKEN Center for Sustainable Resource Sciences, Suehiro-cho-1-7-22, Tsurumi Ward, Yokohama <br> † These authors contributed equally to this work"
affiliations:
 - name: "RIKEN Center for Integrative Medical Sciences, Suehiro-cho-1-7-22, Tsurumi Ward, Yokohama, Kanagawa 230-0045, Japan"
   index: 1
 - name: "RIKEN Center for Sustainable Resource Sciences, Suehiro-cho-1-7-22, Tsurumi Ward, Yokohama, Kanagawa 230-0045, Japan"
   index: 2
date: "Friday 21 May 2021"
output:
  prettydoc::html_pretty:
       theme: cayman
       number_sections: true
       toc: true
       toc_depth: 4
       keep_html: true
       keep_md: true
toc-title: "Table of Contents"
tags:
  - single-cell
  - next-generation-sequencing
  - UMI-tools
  - genomics
  - gene-expression
  - scRNA-Seq
  - bioinformatics
  - data-processing
---


![Docker Manual build](https://img.shields.io/docker/automated/tomkellygenetics/universc?label=docker%20local%20build)
![Docker Cloud Build](https://img.shields.io/docker/cloud/automated/tomkellygenetics/universc?label=docker%20cloud%20build)
![Docker Cloud Status](https://img.shields.io/docker/cloud/build/tomkellygenetics/universc?label=cloud%20build)
![Docker Stars](https://img.shields.io/docker/stars/tomkellygenetics/universc)
![Docker Pulls](https://img.shields.io/docker/pulls/tomkellygenetics/universc)

![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/tomkellygenetics/universc/1.1.1)
![MicroBadger Layers (latest)](https://img.shields.io/microbadger/layers/tomkellygenetics/universc/latest?label="layers@1.1.1")
![Docker Image Size (v1.1.1)](https://img.shields.io/docker/image-size/tomkellygenetics/universc/1.1.1?label="image%20size@1.1.1)
![Docker Image Version (latest by date)](https://img.shields.io/docker/v/tomkellygenetics/universc/latest)
![MicroBadger Layers (latest)](https://img.shields.io/microbadger/layers/tomkellygenetics/universc/latest)
![Docker Image Size (latest)](https://img.shields.io/docker/image-size/tomkellygenetics/universc/latest)

![GitHub branch checks state](https://img.shields.io/github/checks-status/minoda-lab/universc/master?label=GitHub%20checks)
![GitHub Release Date](https://img.shields.io/github/release-date/minoda-lab/universc)
![GitHub last commit (branch)](https://img.shields.io/github/last-commit/minoda-lab/universc/master)
![GitHub issues](https://img.shields.io/github/issues/minoda-lab/universc)
![GitHub pull requests](https://img.shields.io/github/issues-pr/minoda-lab/universc)

[![GitHub Views](http://hits.dwyl.com/minoda-lab/universc.svg)](http://hits.dwyl.com/minoda-lab/universc)
[![GitHub Views](http://hits.dwyl.com/tomkellygenetics/universc.svg)](http://hits.dwyl.com/tomkellygenetics/universc)
![GitHub search hit counter](https://img.shields.io/github/search/minoda-lab/universc/master)
![GitHub forks](https://img.shields.io/github/forks/minoda-lab/universc?style=social)
![GitHub Repo stars](https://img.shields.io/github/stars/minoda-lab/universc?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/minoda-lab/universc?style=social)

![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/minoda-lab/universc)
![GitHub repo size](https://img.shields.io/github/repo-size/minoda-lab/universc)
![GitHub top language](https://img.shields.io/github/languages/top/minoda-lab/universc)
![GitHub language count](https://img.shields.io/github/languages/count/minoda-lab/universc)

![GitHub all releases](https://img.shields.io/github/downloads/minoda-lab/universc/total?label=GitHub%20downloads)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/minoda-lab/universc?label=GitHub%20release)
![GitHub release (latest by date)](https://img.shields.io/github/downloads/minoda-lab/universc/1.1.1/total)
![GitHub release (by tag)](https://img.shields.io/github/downloads/minoda-lab/universc/1.1.1/total)

![Docker CI](https://github.com/minoda-lab/universc/workflows/CI%20to%20Docker%20hub/badge.svg)
![Docker compose](https://github.com/minoda-lab/universc/workflows/Docker%20compose%20build/badge.svg)
![Actions Build](https://github.com/minoda-lab/universc/workflows/Docker%20container%20tests/badge.svg)
![Actions Call](https://github.com/minoda-lab/universc/workflows/Docker%20build%20image/badge.svg)

![Actions Tests](https://github.com/minoda-lab/universc/workflows/Run%20all%20tests%20in%20Docker/badge.svg)
![Test 10x Genomics](https://github.com/minoda-lab/universc/workflows/Test%2010x%20Genomics/badge.svg)
![Test DropSeq](https://github.com/minoda-lab/universc/workflows/Test%20DropSeq%20%2F%20Nadia/badge.svg)
![Test ICELL8](https://github.com/minoda-lab/universc/workflows/Test%20ICELL8/badge.svg)
![Test SCI-Seq](https://github.com/minoda-lab/universc/workflows/Test%20SCI%2DSeq/badge.svg)
![Test inDrops v3](https://github.com/minoda-lab/universc/workflows/Test%20inDrops%20v3/badge.svg)
![Test Smart-Seq3](https://github.com/minoda-lab/universc/workflows/Test%20Smart%2DSeq3/badge.svg)

# UniverSC

**Single-cell processing across technologies**

------------------------------------------

**Summary**

Single-cell RNA-sequencing analysis to quantify RNA molecules in individual cells has become popular owing to 
the large amount of information one can obtain from each experiment. UniverSC is a universal single-cell processing 
tool that supports any UMI-based platform. Our command-line tool enables consistent and comprehensive integration,
comparison, and evaluation across data generated from a wide range of platforms. Here we provide a guide to install
and use this tool to process single-cell RNA-Seq data from FASTQ format.

**Package**

UniverSC version 1.1.1

**Maintainers**

Tom Kelly^†^ (RIKEN IMS) and Kai Battenberg^†^ (RIKEN CSRS/IMS)

† These authors contributed equally to this work

Contact: &lt;first name&gt;.&lt;family name&gt;[at]riken.jp

------------------------------------------

**Disclaimer**: we are third party developers not affiliated with 10X Genomics or any other vendor of single-cell technologies.
We are releasing this code on an open-source [license](#licensing) which calls Cell Ranger™ as an external dependency.

------------------------------------------

## Getting Started

### Advanced users

If you have `cellranger` already installed, then all you need to do is clone or download this git repository. You can then run the script in this directory or add it your `PATH`. See the [Quick Start](#quick-start) guide below.

If you wish to install `cellranger` and configure this script to run on a Linux environment, we provide details on [installation](#installation) below. Note that `launch_universc.sh` requires write-access a Cell Ranger installation so it needs to be installed in a user's "home" directory on a server. No admin powers needed!

Note that `cellranger` installations that are pre-compiled on Linux will not run on Mac or Windows. Note that Mac OS and some Linux distributions also have different version of sed and rename. It is possible to compile an open-source version of Cell Ranger but it is tricky to install the dependencies so we recommend using our docker [image](#Docker) if you wish to do this. 

### Beginners

If you are a beginner bioinformatician or wish to run this on a local computer (Mac or Windows), no problem! We provide a "docker" image containing everything needed to run it without installing the software needed. All you need to do is install [docker](https://docs.docker.com/desktop/) and follow our guide to use the [image](#Docker). This comes bundled with all the compatible versions needed to run it.

Note that you need to run the shell commands given in a unix-like command-line interface (the "Terminal" application on Mac or Linux systems). Many shells are supported but we recommend the "bash" shell for beginners (this is the default on most systems). Windows 10 includes a [subsystem](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to run `bash`. If this is too complicated, you can open a Linux environment (Ubuntu) in docker by following our instructions. Then you can enter bash commands into the terminal opened by docker.

If you run into problems installing or running `launch_universc.sh` please don't hesistate to contact us via email or GitHub.


## Purpose

We've developed a bash script that will run Cell Ranger on FASTQ files for these technologies. See below for details on how to use it.

If you use this tool, please [cite](#Citation) to acknowledge the efforts of the authors. You can report problems and request
new features to the maintainers with and [issue](#Issues) on GitHub. Details on how to [install](#Install) and [run](#Usage) are provided
below. Please see the [help](#Help) and [examples](#Examples) to try solve your problem before submitting an issue.

Details on the [Docker image](#Docker) are given below. We recommend using Docker unless you have a server environment with Cell Ranger installed already.

### Supported Technologies

In principle, any technology with a cell barcode and unique molecular identifier (UMI) can be supported.

The following technologies have been tested to ensure that they give the expected results: 10x Genomics, Nadia (DropSeq), ICELL8 version 3 

We provide the following preset configurations for convenience based on published data and configurations used by other pipelines 
(e.g, DropSeqPipe and Kallisto/Bustools). To add further support for other technologies or troubleshoot problems, please submit an Issue
to the GitHub repository: [minoda-lab/universc](https://github.com/minoda-lab/universc/issues)
as described in [Bug Reports](#Issues) below.

Some changes to the Cell Ranger install are required to run other technologies. Therefore we provide settings for 10x Genomics
which restores settings for the Chromium instrument. We therefore recommend using 'convert' for processing all data from different
technologies as the tool manages these changes. Please note that on a single install of Cell Ranger, multiple technologies or multiple samples 
of the same technology with different whitelist barcodes cannot be run cannot be run simultaneousely (the tool will also check for this to
avoid causing problems with existing runs). Multiple samples of the same technology with the same barcode whitelist can be run simultaneously.

If you are using `UniverSC` you should also do so to run 10x Genomics data. If you wish to restore Cell Ranger to
default settings, see the [installation](#Uninstalling) or [troubleshooting](#Debugging) sections below. 

#### Pre-set configurations

-  10x Genomics (version automatically detected): 10x, chromium
    -  10x Genomics version 2 (16 bp barcode, 10 bp UMI): 10x-v2, chromium-v2
    -  10x Genomics version 3 (16 bp barcode, 12 bp UMI): 10x-v3, chromium-v3
-  Aligent Bravo B (16 bp barcode, No UMI): aligent, bravo 
-  BD Rhapsody (27 bp barcode, 8 bp UMI): bd-rhapsody
-  CEL-Seq
    -  CEL-Seq  (8 bp barcode, 4 bp UMI): celseq
    -  CEL-Seq2 (6 bp UMI, 6 bp barcode): celseq2
-  Drop-Seq (12 bp barcode, 8 bp UMI): dropseq
-  ICELL8
    -  ICELL8 version 2 (11 bp barcode, No UMI): icell8-non-umi, icell8-v2
    -  ICELL8 version 3 (11 bp barcode, 14 bp UMI): icell8 or custom
    -  ICELL8 5′ scRNA with TCR OR kit (10bp barcode, NO bp UMI): icell8-5-prime
    -  ICELL8 full-length scRNA with Smart-Seq (16 bp barcode, No UMI): icell8-full-length
-  inDrops
    -  inDrops version 1 (19 bp barcode, 6 bp UMI): indrops-v1, 1cellbio-v1
    -  inDrops version 2 (19 bp barcode, 6 bp UMI): indrops-v2, 1cellbio-v2
    -  inDrops version 3 (16 bp barcode, 6 bp UMI): indrops-v3, 1cellbio-v3
 -  MARS-Seq
    -  MARS-Seq  (6 bp barcode, 10 bp UMI): marsseq, marsseq-v1
    -  MARS-Seq2 (7 bp barcode, 8 bp UMI): marsseq2, marsseq-v2   
-  Microwell-Seq (18 bp barcode, 6 bp UMI): microwell
-  Nadia (12 bp barcode, 8 bp UMI): nadia, dropseq
-  Quartz-Seq
    -  QuartzSeq (6 bp index, no UMI): quartz-seq
    -  Quartz-Seq2 (14 bp barcode, 8 bp UMI): quartzseq2-384
    -  Quartz-Seq2 (15 bp barcode, 8 bp UMI): quartzseq2-1536
-  RamDA-Seq (6 bp index, no UMI): ramda-seq
-  Single-cell combinatorial indexing (SCI-RNA-Seq)
   -  SCI-Seq 2-level indexing (30 bp barcode, 8 bp UMI): sciseq2
   -  SCI-Seq 3-level indexing (40 bp barcode, 8 bp UMI): sciseq3
   -  SCIFI-Seq (27 bp barcode, 8 bp UMI): scifiseq
-  SCRB-Seq (6 bp barcode, 10 bp UMI): scrbseq, mcscrbseq
-  SeqWell (12 bp barcode, 8 bp UMI): plexwell, seqwell, seqwells3
-  SPLiT-Seq (10 bp UMI, 24 bp barcode): splitseq
-  Smart-seq
   -  Smart-Seq (16 bp barcode, No UMI): smartseq
   -  Smart-Seq2 (16 bp barcode, No UMI): smartseq2
   -  Smart-Seq2-UMI, Smart-seq3 (16 bp barcode, 8 bp UMI): smartseq3
-  STRT-Seq
    -  STRT-Seq (6 bp barcode, no UMI)
    -  STRT-Seq-C1 (8 bp barode, 5 bp UMI)
    -  STRT-Seq-2i (13 bp barcode, 6 bp UMI)
-  SureCell (18 bp barcode, 8 bp UMI): surecell, ddseq, biorad

#### Chemistry settings available

All technologies support 3′ single-cell RNA-Seq. Barcode adjustments and
whitelists are changed automatically. For 5′ single-cell RNA-Seq, this
is only supported for 10x Genomics version 2 chemistry, ICELL8, 
Smart-Seq, and STRT-Seq.
For 10x Genomics, this is detected automatically but can be
configured with the `--chemistry` argument.
For other technologies, the template switching oligonucleotide
is automatically converted to the match the 10x sequence. 

#### Support for UMI-based and non-UMI technologies 

By default, UMIs are supported where available so with the following
exceptions for non-UMI technologies:
ICELL8 v2, RamDA-Seq, Quartz-Seq, Smart-Seq, Smart-Seq2.
While using UMI is recommended we provide a mock UMI for counting
reads for these technologies (and data from previous versions).

Other techniques can be forced to replace the UMI with a mock sequence
for counting reads only with `--non-umi` or `--read-only` arguments.
Forcing non-UMI techniques is _not recommended_ unless you are 
integrating non-UMI and UMI-based technologies. It is not necessary
to specific `--non-umi` for non-UMI techniques as these will be used
automatically when applicable. For ICELL8 and Smart-Seq where both
non-UMI (icell8-v2, smartseq2) and UMI-based (icell8-v3, smartseq3)
techniques are available it is possible to specify which to use.

#### Single and dual indexed technologies

Where needed the cell barcode can be detected in the index I1 or I2 file.
Single indexes are supported for STRT-Seq and Quartz-Seq.
Dual indexes are supported for Fluidigm C1, ICELL8 full-length, 
inDrops-v3, RamDA-Seq, SCI-RNA-Seq, scifi-seq, and Smart-Seq.
Combinatorial indexing technologies have linkers between barcodes removed
automatically to match the barcode whitelist.

#### Demultiplexing for dual-indexing

For dual-indexed technologies such as Fluidigm C1, inDrops-v3, Sci-Seq,
SmartSeq3 it is advised to use "bcl2fastq" before calling UniverSC:

```
   /usr/local/bin/bcl2fastq  -v --runfolder-dir "/path/to/illumina/bcls"  --output-dir "./Data/Intensities/BaseCalls"\
                                --sample-sheet "/path/to/SampleSheet.csv" --create-fastq-for-index-reads\
                                --use-bases-mask Y26n,I8n,I8n,Y50n  --mask-short-adapter-reads 0\
                                --minimum-trimmed-read-length 0
```

Please adjust the lengths for `--use-bases-mask` accordingly for read 1, index 1 (i7), index 2 (i5), and read 2.
Ensure that `--create-fastq-for-index-read` is used where possible.
Using `--no-lane-splitting` is optional as UniverSC can process an arbirtary number of lanes.
There is no need to specify index sequences in the same sheet for cell barcodes, using "NNNNNNNN" will match all
samples and the cell barcodes will be distinguished by the single-cell processing pipeline. Index sequences should
only be used to demultiplex samples and replicates (not cells).

#### Missing index sequences

If a sequencing facility has demultiplexed the samples for you without this,
UniverSC will attempt to extract index sequences from FASTQ headers in read 1.
If index sequences are not stored in the file headers and samples have already
been demultiplexed, a dummy index file of the same number of reads as R1 and R2
will be required. As a workaroudn, you can generate this by copying the R1 and R2
files and replacing the sequences with the first barcode in the relevant whitelist.
For example:

```
index1="TAAGGCGA"
index2="AAGGAGTA"

# create new files
cp R1_file.fastq I1_file.fastq
cp R2_file.fastq I2_file.fastq

# replace sequences
sed -i "2~4s/^.*$/${index1}/g" I1_file.fastq
sed -i "2~4s/^.*$/${index2}/g" I2_file.fastq

# replace quality scores
sed -i "4~4s/^.*$/IIIIIIII/g" I1_file.fastq I2_file.fastq
```

This results in a new "sample index" for each demultiplexed sample.
To combine demultiplexed sampls for dual indexed techniques use the following:

```
# for fastq files
cat Sample1_R1_file.fastq Sample2_R1_file.fastq Sample3_R1_file.fastq > Combined_R1_file.fastq
cat Sample1_R2_file.fastq Sample2_R2_file.fastq Sample3_R2_file.fastq > Combined_R2_file.fastq
cat Sample1_I1_file.fastq Sample2_I1_file.fastq Sample3_I1_file.fastq > Combined_I1_file.fastq
cat Sample1_I2_file.fastq Sample2_I2_file.fastq Sample3_I2_file.fastq > Combined_I2_file.fastq

# for compressed files (not need to uncompress)
cat Sample1_R1_file.fastq.gz Sample2_R1_file.fastq.gz Sample3_R1_file.fastq.gz > Combined_R1_file.fastq.gz
cat Sample1_R2_file.fastq.gz Sample2_R2_file.fastq.gz Sample3_R2_file.fastq.gz > Combined_R2_file.fastq.gz
cat Sample1_I1_file.fastq.gz Sample2_I1_file.fastq.gz Sample3_I1_file.fastq.gz > Combined_I1_file.fastq.gz
cat Sample1_I2_file.fastq.gz Sample2_I2_file.fastq.gz Sample3_I2_file.fastq.gz > Combined_I2_file.fastq.gz
```

As this needs to done on a case-by-case basis it has not been implemented by the UniverSC core functions.
We provide this workaround for using published data and data already processed by sequencing facilities.
Please contact the maintainers or file an issue on GitHub if you are having problems with this case.


#### Custom inputs

Custom inputs are also supported by giving the name "custom" and length of barcode and UMI separated by a "_" character.

 e.g. Custom (16bp barcode, 10bp UMI): `custom_16_10`

Custom barcode files are also supported for preset technologies. These are particularly useful for well-based
technologies to demutliplex based on the wells.

Note that custom inputs do not remove linker or adapter sequences for combinatorial indexng technologies.
These must be removed from the Read 1 file before running UniverSC. To request a preset technology
setting instead, please submit a feature request on GitHub as described below.

## Release

This tool will be released open-source (see [legal stuff](#licensing) below).
We welcome any feedback on it and any contributions to improve it.
Hopefully it will save people time by making it easier to compare technologies.

We have tested it on several technologies but we need users like you
to let us know how we can improve it. We hope that it will save you
time by handing tedious parts of data formatting so that you can
focus on the results.

### Citation <span id="Citation"><span>

A submission to a journal and biorXiv is in progress. Please cite these when
they are available. Currently, the package can be cited
as follows:

Kelly, S.T., Battenberg, Hetherington, N.A., K., Hayashi, K., and Minoda, A. (2021)
UniverSC: a flexible cross-platform single-cell data processing pipeline.
bioRxiv 2021.01.19.427209; doi: [https://doi.org/10.1101/2021.01.19.427209](https://doi.org/10.1101/2021.01.19.427209)
package version 1.1.1. [https://github.com/minoda-lab/universc](https://github.com/minoda-lab/universc)

```
@article {Kelly2021.01.19.427209,
        author = {Kelly, S. Thomas and Battenberg, Kai and Hetherington, Nicola A. and Hayashi, Makoto and Minoda, Aki},
        title = {{UniverSC}: a flexible cross-platform single-cell data processing pipeline},
        elocation-id = {2021.01.19.427209},
        year = {2021},
        doi = {10.1101/2021.01.19.427209},
        publisher = {Cold Spring Harbor Laboratory},
        abstract = {Single-cell RNA-sequencing analysis to quantify RNA molecules in individual cells has become popular owing to the large amount of information one can obtain from each experiment. We have developed UniverSC (https://github.com/minoda-lab/universc), a universal single-cell processing tool that supports any UMI-based platform. Our command-line tool enables consistent and comprehensive integration, comparison, and evaluation across data generated from a wide range of platforms.Competing Interest StatementThe authors have declared no competing interest.},
        eprint = {https://www.biorxiv.org/content/early/2021/01/19/2021.01.19.427209.full.pdf},
        journal = {{bioRxiv}},
        note = {package version 1.1.1},
        URL = {https://github.com/minoda-lab/universc},
}

```

```
@Manual{,
    title = {{UniverSC}:  a flexible cross-platform single-cell data processing pipeline},
    author = {S. Thomas Kelly, Kai Battenberg, Nicola A. Hetherington, Makoto Hayashi, and Aki Minoda},
    year = {2021},
    note = {package version 1.1.1},
    url = {https://github.com/minoda-lab/universc},
  }
```

### Bug Reports <span id="Issues"><span>

#### Reporting issues

To add further support for other technologies or troubleshoot problems, please submit an Issue 
to the GitHub repository: https://github.com/minoda-lab/universc/issues

Please submit [issues](https://github.com/minoda-lab/universc/issues) on GitHub to report
problems or suggest features. [Pull requests](https://github.com/minoda-lab/universc/pulls)
to the `dev` branch on GitHub are also welcome to add features or correct problems. Please see
the [contributor guide](CONTRIBUTING.md) for more details.

### Requesting new technologies

Where possible, please provide an minimal example of the first few lines of each FASTQ file for testing purposes.

It is also helpful to describe the technology, such as:

- length of barcode
- length of UMI
- which reads they're on
- whether there is a known barcode whitelist available
- whether adapters or linkers are required
- whether a preprint, publication, or company specifications are available

Technologies that may be difficult to support are those with:

- barcodes longer than 16bp
- barcodes with phase blocks or varying length
- UMIs longer than 12bp
- technologies that do not have UMI
- combinatorial indexing
- dual indexing

Please bear this in mind when submitting requests. We will consider to add further technologies but
it could take significant resources to add support for techniques with these designs.
Note that updates to the tool have added support for several examples of these.

## Installation <span id="installation"><span>

This script requires Cell Ranger to be installed and exported to the PATH (version 3.0.0 or higher recommended).
The script itself is exectuable and does not require installation to run but you can put it in your PATH or
bin of your Cell Ranger install if you wish to do so. We provide scripts to do this for your convenience.

See the details below on how set up Cell Ranger and launch_universc.sh.

#### Download UniverSC

To download UniverSC open a terminal prompt and enter the following commands.

```
cd $HOME/Downloads
git clone https://github.com/minoda-lab/universc.git
cd universc
```

### Quick Start

If you already have Cell Ranger installed, then you can run the script without installing it.

```
bash launch_universc.sh
```

You can call it in another directory by giving the path to the script.

```
cd $/HOME/my_project
bash $HOME/Downloads/universc/launch_universc.sh
```

See the details below on how to install Cell Ranger and launch_universc.sh add them
to the PATH so that `launch_universc.sh` can be run from any directory. 

### Runnning in a git repository

If you are running code in a git repository you can add UniverSC as a submodule.

```
cd $/HOME/my_git_repo
git submodule add https://github.com/minoda-lab/universc.git
bash universc/launch_universc.sh
```

### System Requirements

In principle, the script can run on any Unix systems with Cell Ranger installed. You can check whether
Cell Ranger is already availble by running:

```
whereis cellranger
```

You can see which Cell Ranger installation will run as follows:

```
which cellranger
cellranger count --version
```

If Cell Ranger is already installed on your system, you can add it to your $PATH as follows:

```
export PATH=/home/username/path/to/cellranger-x.x.x:$PATH    
```

#### Installing dependencies

If Cell Ranger is not installed on your system, you must install it before running launch_universc.sh.

Please see the [manual for Cell Ranger](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/what-is-cell-ranger)
on the 10x Genomics website for more details on how to use it. We provide support for
passing various options to Cell Ranger and sensible defaults for each technology.

This script is compatible with the installation of Cell Ranger that you can
[download](https://support.10xgenomics.com/single-cell-gene-expression/software/downloads/latest)
from the 10x Genomics website and gives the same output formats.

However, we recommend to use the open-source release of Cell Ranger on GitHub. This is
release on an MIT License and is not subject to the 10x Genomics End User
License Agreement.

We provide open-source repositories with minor updates for compatibility
with current versions of dependencies.

The code is available here:

[https://github.com/minoda-lab/cellranger/releases](https://github.com/minoda-lab/cellranger/releases)

We also provide Docker images for Cell Ranger versions 2.0.2, 2.1.0, 2.1.1, and 3.0.2:

[https://github.com/minoda-lab/cellranger_clean/packages](https://github.com/minoda-lab/cellranger_clean/packages)

[https://hub.docker.com/r/tomkellygenetics/cellranger_clean/tags](https://hub.docker.com/r/tomkellygenetics/cellranger_clean/tags)

#### Cluster Mode configuration

#### Software Requirements

These have been pre-installed in the Docker image described above.

A full example of installation is available in the [GitHub repository](https://github.com/minoda-lab/cellranger)
and on [DockerHub](https://hub.docker.com/r/tomkellygenetics/cellranger_clean/dockerfile).

- Python 2.7.13
- rust 1.28.0
- clang 6.0
- go 1.11
- node 8.11.4
- Cython 0.28.0
- STAR 2.5.1b
- bcl2fastq 2.19.1.403
- tsne 0.15

The following additional shell utilities are required. Mac OS and
most Linux distributions come with these pre-installed.

- make 3.81
- git 2.20.1 
- sed (GNU sed) 4.4 (gsed)
- tar  2.8.3
- rename 0.20 (perl-rename)
- perl 5.26.1
- rsync 2.6.9 

Note that rename is installed by default on Mac, Ubuntu and Debian
but a different version must be used on other Linux distrubutions.

CentOS and Fedora:

```
sudo yum install prename
```
```
sudo dnf install prename
```

Red Hat Linux:

```
sudo rpm install prename
```

Arch Linux:

```
yay perl-rename
```

##### Recommended software

- git-lfs 2.10.0

#### Hardware requirements

- 8-core Intel or AMD processor (16 cores recommended)
- 64GB RAM (128GB recommended)
- 1TB free disk space
- 64-bit CentOS/RedHat 6.0 or Ubuntu 12.04

#### Ensuring write-access to Cell Ranger

The conversion process requires write-access to to the Cell Ranger install directory so
an install on your user directory is recommended. 

You can check where Cell Ranger is installed with:

```
which cellranger
```

If calling the script gives the help menu, launch_universc.sh has sucessfully run
with access to the directories that it needs. It will give an error
message if the Cell Ranger directory is not writeable.

```
bash launch_universc.sh
```

This script requires Cell Ranger (version 3.0.0 or higher recommended) to be installed and have write-access
to the Cell Ranger install directory, so an install on your user directory is recommended.
This script also requires Cell Ranger to be exported to the PATH.
The script itself is exectuable and does not require installation to run but you can put it
in your PATH or bin of your Cell Ranger install if you wish to do so.

This script will run in bash on any OS (but it has only been tested on Linux Debian). Running Cell Ranger 
with this configuration requires a lot of memory (40Gb) so running on server is recommended.
SGE job modes are supported to run Cell Ranger with multiple threads.

This is required because launch_universc.sh will make changes to the Cell Ranger install
to ensure compatibility with the technology running. A local install in
you user home directory is needed to make these changes. This ensures
that these changes do not affect jobs run by other users and allows
launch_universc.sh to change the whitelist and source code as needed.

These changes are reversible but mean that only one technology can be
run at the same time. You can restore original configurations with:

```
bash launch_universc.sh -t "10x" --setup
```

##### Local install

If Cell Ranger is not already installed we recommend installing it in a directory that
you have write access to such as `$HOME/local`.

##### Importing an installed version of Cell Ranger

If Cell Ranger has been installed by a system administrator, you will only have read-access
to that installation. You can still use rather than installing a new version but you
will need to copy it to your home directory and add this version to your PATH.

```
mkdir -p $HOME/local
cd ~/local
installed_version=$(echo $(which cellranger) | rev | cut -d"/" -f2- | rev)
cp -rv $installed_version  .
installed_directory=$(echo $(which cellranger) | rev | cut -d"/" -f2 | rev) 
cd $installed_directory
new_version=$(pwd)
#remove previous version from PATH
export PATH=$(echo $PATH |  sed "s;$installed_version:;;g")
#add new version to PATH
eval $(echo export PATH=$new_version:\$PATH)
cd ..
```

You should be able to see that the locally installed version can be called as follows:

```
echo $PATH
which cellranger
bash launch_universc.sh
```

#### Installing launch_universc.sh to the PATH

##### Running the script

Adding the script to the PATH is not absolutely neccessary, it can
be called as follows from the directory that it is downloaded in.

```
cd $HOME/Downloads
git clone https://github.com/minoda-lab/universc.git
cd universc
bash launch_universc.sh
```

##### Automated configuration

We provide a Makefile with all necessary configurations to automatically
check whether launch_universc.sh is installed correctly.

You can specify any directory to install as a "prefix". This will
create a directory "$HOME/local/universc-0.3" where
the files needed will be stored.

```
cd $HOME/Downloads
git clone https://github.com/minoda-lab/universc.git
make
make install prefix=$HOME/local
```

It is also possible to add the current working directory as 
the installed directory.

```
make install prefix="."
```

In this case *do not* delete the installed directory after you
install it or the script will fail to run.

By default it will be installed in a root directory with
read-only access. This requires administrator priviledges.
Note that the manual can onlly be installed with root
priviledges.

```
sudo make install
sudo make manual
```

You can verify that launch_universc.sh has been added to the PATH.

```
echo $PATH
which launch_universc.sh
```

You can then run `launch_universc.sh` from any working directory.

##### Updating

If launch_universc.sh is already installed and you wish to update it,
first you need to pull the changes from GitHub from the
universc directory.

```
cd universc
git pull origin master
make
```

Then you can update to the directory of your choice using
the same options for `--prefix` as to install.

```
make install prefix=$HOME/local
```

This is remove previous versions of launch_universc.sh and install
the latest version.

The manual can be updated with:

```
sudo make manual
```

##### Uninstalling

Before uninstalling UniverSC please ensure that any
versions of Cell Ranger used are restored to their default configuration:

```
export PATH=/Users/tom/Downloads/cellranger-x.y.z:$PATH
bash launch_universc.sh -t "10x" --setup
```

We provide an automated script to reverse the changes above.

```
make uninstall
```

This is will automatically detect the installation of launch_universc.sh.

If multiple versions of Cell Ranger are present, you can
specify which to remove with.

```
make remove prefix=$HOME/local
```

#### Custom shell

Make will install the script with `bash` by default but
alternative shells are supported. You will need to run the
install script or run it with your shell of choice.

```
sh launch_universc.sh
sh inst/INSTALL --prefix $HOME/local
launch_universc.sh
```

```
ksh launch_universc.sh
ksh inst/INSTALL --prefix $HOME/local
launch_universc.sh
```

```
zsh launch_universc.sh
zsh inst/INSTALL --prefix $HOME/local
launch_universc.sh
```

```
fish launch_universc.sh
fish inst/INSTALL --prefix $HOME/local
launch_universc.sh
```

The help menu should reflect the shell used to run it.

To update, similarly run the `inst/UPGRADE` script with
your chosen shell.

### Docker image <span id="Docker"><span>

We provide a docker image with all software needed
to run UniverSC.

This requires "docker" to be installed and a valid DockerHub account.

You can check whether docker is available by running:

```
which docker
docker run hello-world    
```

This may require you to login to your account.

```
docker login -u "myusername"
```

If you cannot run docker on a remote server, contact
your systems administrator.

#### Pulling from remote DockerHub repository

We provide a docker image for UniverSC version 1.1.1.

You can import it if you have docker installed.

```
docker pull tomkellygenetics/universc:latest
```

Then you can run convert with:

```
run -it tomkellygenetics/universc:latest launch_universc.sh
```

You can open a shell in the docker image with:

```
run -it tomkellygenetics/universc:latest /bin/bash
```

```
run -it tomkellygenetics/universc:latest /bin/zsh 
```

Either of these shells are supported.

##### Building the Docker image locally

The Dockerfile is provided in the repository so it can be built from
source. This will build a Docker image with the latest version of
universc provided that updates to dependencies on GitHub
are still compatible.

```
git clone https://github.com/minoda-lab/universc.git
docker build -t universc:latest .  
```

Please bear mind that it can take considerable time to install
all necessary dependencies. A stable internet connection is required.

### Manual configuration

You can manually add the script here to the PATH, for example:

```
PATH=$HOME/Downloads/universc:$PATH
```

This means that the directory where the script is can be found
from the shell.

```
echo $PATH
cd ~
launch_universc.sh
```

Add the following line to the `~/.bashrc` file and use `source ~/.bashrc`
to load a new session. This means that you do not need to add the
sript to the PATH in future sessions.

```
export PATH=$HOME/Downloads/universc:$PATH
```

### Setting up Cell Ranger references

This repository comes with almost all necessary files to run test jobs. Test data and
Cell Ranger references are available with Git large file storage (LFS).

To install git LFS run:

```
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
git lfs install
```

To import large files from Github change to the "universc" directory and run:

```
git lfs pull origin
```

This provides almost all files required. The STAR index and reference need to be generated or
imported from an existing reference. The following code detects whether the references are
available in an existing cellranger installation.

```
cellrangerversion=`cellranger count --version | head -n 2 | tail -n 1 | cut -f2 -d'(' | cut -f1 -d')'`
cellrangerpath=`which cellranger`

# set up cellranger reference
if [[ ! -f test/cellranger_reference/cellranger-tiny-ref/3.0.0/star/SA ]] && [[ -f $(dirname $cellrangerpath)/cellranger-tiny-ref/3.0.0/star/SA ]]; then
    rsync $(dirname $cellrangerpath)/cellranger-tiny-ref/3.0.0/star/SA test/cellranger_reference/cellranger-tiny-ref/3.0.0/star/SA
fi
if [[ ! -f test/cellranger_reference/cellranger-tiny-ref/1.2.0/star/SA ]] && [[ -f $(dirname $cellrangerpath)/cellranger-tiny-ref/1.2.0/star/SA ]]; then
    rsync $(dirname $cellrangerpath)/cellranger-tiny-ref/1.2.0/star/SA test/cellranger_reference/cellranger-tiny-ref/1.2.0/star/SA
fi
```

This creates a reference for Cell Ranger here:

- test/cellranger_reference/cellranger-tiny-ref/1.2.0

- test/cellranger_reference/cellranger-tiny-ref/3.0.0


#### Automated references

You can reset the references with the automated settings here:

```
cd test/cellranger_reference/cellranger-tiny-ref/
make clean
make reference
cd ../../..
```

#### Custom Cell Ranger references

It is also possible to generate a custom reference for any genome provided you have
a FASTQ genome reference file and a GTF/GFF3 annotation file. Please ensure that the
chromosomes match between the FASTA headers and the chromosome column (1st) of the
GTF/GFF3 file.

The `gffread` function includes with the [cufflinks](http://cole-trapnell-lab.github.io/cufflinks/file_formats/#the-gffread-utility)
utility can convert to gtf. For example:

```
gffread test/cellranger_reference/cellranger-tiny-ref/genes-1.2.0.gff3 -T -o test/cellranger_reference/cellranger-tiny-ref/genes-1.2.0.gtf 
```

To generate new references we first remove the references imported.

```
rm -rf test/cellranger_reference/cellranger-tiny-ref/1.2.0 test/cellranger_reference/cellranger-tiny-ref/3.0.0
```

We then generate references from the FASTA and GTF files as shown in the following examples:

```
cellranger mkref --genome=test/cellranger_reference/cellranger-tiny-ref/1.2.0 \
        --fasta=test/cellranger_reference/cellranger-tiny-ref/genome-1.2.0.fa \
        --genes=test/cellranger_reference/cellranger-tiny-ref/ genes-1.2.0.gtf

cellranger mkref --genome=test/cellranger_reference/cellranger-tiny-ref/3.0.0 \
         --fasta=test/cellranger_reference/cellranger-tiny-ref/genome-3.0.0.fa \
         --genes=test/cellranger_reference/cellranger-tiny-ref/ genes-3.0.0.gtf
```

See the Cell Ranger manuals for more [details on references](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/advanced/references). 

## Usage <span id="Usage"><span>

The script will:

- give you a help guide

`bash launch_universc.sh -h`

- convert R1 files so that barcodes and UMIs are where they're expected to be for 10x (this can take some time for larger files)

- runs Cell Ranger with the same parameters as for 10x and treats samples exactly the same

- the barcode whitelists are changed and some checks on barcodes disabled (requires a writeable install of Cell Ranger in your user directory)

- it can run Cell Ranger in parallel in SGE mode on the server if you use `--jobmode "sge"` and set up an `sge.template` file

- it can also restore the original Cell Ranger settings for running 10x samples

`bash launch_universc.sh --setup --technology "10x"`

### Valid barcodes

Please note that this script alters the barcode whitelist. Known ICELL8 barcodes are supported but this is not possible with Nadia or DropSeq chemistry so 100% valid barcodes will be returned.

### Manual <span id="Help"><span>

#### Locally install manual

You can display a manual from the locally installed UniverSC directory with:

```
 man man/launch_universc.sh 
```

Note that the working directory must be `universc` or the full path to the man directory must be given.

#### Installing the manual with root priviliges:

##### Automated Configuration

We provide an automated script to install the manual.

```
sudo make manual
```

You can remove the manual with:

```
sudo make manual-clean
```

##### Configuration

The manual can be installed as follows on Mac and Linux.

```
# add manual directory to PATH if not already found
## check config for Linux
if [[ -f /etc/manpath.config ]]
    then CONFIG="/etc/manpath.config"
fi
## check config for Mac
if [[ -f /etc/manpaths ]]
    then CONFIG="/etc/manpaths"
fi
if [[ ! -z $CONFIG ]]
    then MANDIR=`tail -n 1 ${CONFIG}`
else if [[ ! -z $MANPATH ]]
    then
    SHELL_RC=`echo ~/.${0}rc`
    echo "export MANPATH=/usr/local/man" >> $SHELL_RC
    MANDIR=`echo ${MANPATH} | cut -d: -f1`
    fi
fi
sudo mkdir -p ${MANDIR}/man1
cp man/launch_universc.sh man/launch_universc.sh.1
sudo mv man/launch_universc.sh.1 ${MANDIR}/man1/launch_universc.sh.1
gzip ${MANDIR}/man1/launch_universc.sh.1
```

Alternatively the man can be installed with:

```
cp man/launch_universc.sh man/launch_universc.sh.1
sudo install -g 0 -o 0 -m 0644 man/launch_universc.sh.1 ${MANDIR}/man1
```

The manual can then be called from any directory as follows:

```
man launch_universc.sh
```

#### Help menu

You can access the following help menu with `launch_universc.sh --help` in the terminal.

```
Usage:
  bash launch_universc.sh --testrun -t THECHNOLOGY
  bash launch_universc.sh -t TECHNOLOGY --setup
  bash launch_universc.sh -R1 FILE1 -R2 FILE2 -t TECHNOLOGY -i ID -r REFERENCE [--option OPT]
  bash launch_universc.sh -R1 READ1_LANE1 READ1_LANE2 -R2 READ2_LANE1 READ2_LANE2 -t TECHNOLOGY -i ID -r REFERENCE [--option OPT]
  bash launch_universc.sh -f SAMPLE_LANE -t TECHNOLOGY -i ID -r REFERENCE [--option OPT]
  bash launch_universc.sh -f SAMPLE_LANE1 SAMPLE_LANE2 -t TECHNOLOGY -i ID -r REFERENCE [--option OPT]
  bash launch_universc.sh -v
  bash launch_universc.sh -h

Convert sequencing data (FASTQ) from Nadia or ICELL8 platforms for compatibility with 10x Genomics and run cellranger count

Mandatory arguments to long options are mandatory for short options too.
       --testrun                Initiates a test trun with the test dataset
  -R1, --read1 FILE             Read 1 FASTQ file to pass to Cell Ranger (cell barcodes and umi)
  -R2, --read2 FILE             Read 2 FASTQ file to pass to Cell Ranger
  -I1, --index1 FILE            Index (I1) FASTQ file to pass to Cell Ranger (OPTIONAL)
  -I2, --index2 FILE            Index (I2) FASTQ file to pass to Cell Ranger (OPTIONAL and EXPERIMENTAL)
  -f,  --file NAME              Path and the name of FASTQ files to pass to Cell Ranger (prefix before R1 or R2)
                                  e.g. /path/to/files/Example_S1_L001

  -i,  --id ID                  A unique run id, used to name output folder
  -d,  --description TEXT       Sample description to embed in output files.
  -r,  --reference DIR          Path of directory containing 10x-compatible reference.
  -t,  --technology PLATFORM    Name of technology used to generate data.
                                Supported technologies:
                                  10x Genomics (version automatically detected): 10x, chromium
                                  10x Genomics version 2 (16 bp barcode, 10 bp UMI): 10x-v2, chromium-v2
                                  10x Genomics version 3 (16 bp barcode, 12 bp UMI): 10x-v3, chromium-v3
                                  Aligent Bravo B (16 bp barcode, No UMI): aligent, bravo
                                  BD Rhapsody (27 bp barcode, 8 bp UMI): bd-rhapsody
                                  CEL-Seq (8 bp barcode, 4 bp UMI): celseq
                                  CEL-Seq2 (6 bp UMI, 6 bp barcode): celseq2
                                  Drop-Seq (12 bp barcode, 8 bp UMI): dropseq
                                  ICELL8 version 2 (11 bp barcode, No UMI): icell8-non-umi, icell8-v2
                                  ICELL8 version 3 (11 bp barcode, 14 bp UMI): icell8 or custom
                                  ICELL8 5′ scRNA with TCR OR kit (10bp barcode, NO bp UMI): icell8-5-prime
                                  ICELL8 full-length scRNA with Smart-Seq (16 bp barcode, No UMI): icell8-full-length
                                  inDrops version 1 (19 bp barcode, 6 bp UMI): indrops-v1, 1cellbio-v1
                                  inDrops version 2 (19 bp barcode, 6 bp UMI): indrops-v2, 1cellbio-v2
                                  inDrops version 3 (16 bp barcode, 6 bp UMI): indrops-v3, 1cellbio-v3
                                  Nadia (12 bp barcode, 8 bp UMI): nadia, dropseq
                                  MARS-Seq (6 bp barcode, 10 bp UMI): marsseq, marsseq-v1
                                  MARS-Seq2 (7 bp barcode, 8 bp UMI): marsseq2, marsseq-v2   
                                  Microwell-Seq (18 bp barcode, 6 bp UMI): microwell
                                  QuartzSeq (6 bp index, no UMI): quartz-seq
                                  Quartz-Seq2 (14 bp barcode, 8 bp UMI): quartzseq2-384
                                  Quartz-Seq2 (15 bp barcode, 8 bp UMI): quartzseq2-1536
                                  RamDA-Seq (6 bp index, no UMI): ramda-seq
                                  SCI-Seq 2-level indexing (30 bp barcode, 8 bp UMI): sciseq2
                                  SCI-Seq 3-level indexing (40 bp barcode, 8 bp UMI): sciseq3
                                  SCIFI-Seq (27 bp barcode, 8 bp UMI
                                  SCRB-Seq (6 bp barcode, 10 bp UMI): scrbseq, mcscrbseq
                                  SeqWell (12 bp barcode, 8 bp UMI): plexwell, seqwell, seqwells3
                                  Smart-seq (16 bp barcode, No UMI): smartseq
                                  Smart-seq2 (16 bp barcode, No UMI): smartseq2
                                  Smart-seq2-UMI, Smart-seq3 (16 bp barcode, 8 bp UMI): smartseq3
                                  SPLiT-Seq (10 bp UMI, 24 bp barcode): splitseq
                                  STRT-Seq (6 bp barcode, no UMI)
                                  STRT-Seq-C1 (8 bp barode, 5 bp UMI)
                                  STRT-Seq-2i (13 bp barcode, 6 bp UMI)
                                  SureCell (18 bp barcode, 8 bp UMI): surecell, ddseq, biorad
                                Custom inputs are also supported by giving the name "custom" and length of barcode and UMI separated by "_"
                                  e.g. Custom (16 bp barcode, 10 bp UMI): custom_16_10

  -b,  --barcodefile FILE       Custom barcode list in plain text (with each line containing a barcode)

  -c,  --chemistry CHEM         Assay configuration, autodetection is not possible for converted files: SC3Pv2 (default), SC5P-PE, or SC5P-R2
                                    5′ scRNA-Seq ('SC5P-PE') is available only for 10x Genomics, ICELL8, SmartSeq, and STRT-Seq technologies
                                    All other technologies default to 3′ scRNA-Seq parameters. Only 10x Genomics and ICELL8 allow choosing which to use.
  -n,  --force-cells NUM        Force pipeline to use this number of cells, bypassing the cell detection algorithm.
  -j,  --jobmode MODE           Job manager to use. Valid options: local (default), sge, lsf, or a .template file
       --localcores NUM         Set max cores the pipeline may request at one time.
                                    Only applies when --jobmode=local.
       --localmem NUM           Set max GB the pipeline may request at one time.
                                    Only applies when --jobmode=local.
       --mempercore NUM         Set max GB each job may use at one time.
                                    Only applies in cluster jobmodes.

  -p,  --per-cell-data          Generates a file with basic run statistics along with per-cell data

       --non-umi or --read-only Force counting reads by adding or replacing UMI with a mock sequence

       --setup                  Set up whitelists for compatibility with new technology and exit
       --as-is                  Skips the FASTQ file conversion if the file already exists

  -h,  --help                   Display this help and exit
  -v,  --version                Output version information and exit
       --verbose                Print additional outputs for debugging

For each fastq file, follow the naming convention below:
  <SampleName>_<SampleNumber>_<LaneNumber>_<ReadNumber>_001.fastq
  e.g. EXAMPLE_S1_L001_R1_001.fastq
       Example_S4_L002_R2_001.fastq.gz

For custom barcode and umi length, follow the format below:
  custom_<barcode>_<UMI>
  e.g. custom_16_10 (which is the same as 10x)

Files will be renamed if they do not follow this format. File extension will be detected automatically.

```

### Examples <span id="Examples"><span>

#### Running Cell Ranger

```
cellranger testrun --id="tiny-test"
```
```
# open gzip files from test data
gunzip -fk universc/test/shared/cellranger-tiny-fastq/3.0.0/*fastq.gz
gunzip -fk cellranger-3.0.2.9001/cellranger-cs/3.0.2.9001/lib/python/cellranger/barcodes/3M-february-2018.txt.gz 
# Cell Ranger call
cellranger count --id="tiny-count-v3" \
 --fastqs="cellranger-3.0.2.9001/cellranger-tiny-fastq/3.0.0/" --sample="tinygex" \
 --transcriptome="cellranger-3.0.2.9001/cellranger-tiny-ref/3.0.0"
```

#### Running launch_universc.sh on 10x data

```
# call convert on 10x with multiple lanes
bash /universc/launch_universc.sh --id "test-10x-v3" --technology "10x" \
 --reference "/universc/test/cellranger_reference/cellranger-tiny-ref/3.0.0" \
 --file "/universc/test/shared/cellranger-tiny-fastq/3.0.0/tinygex_S1_L001" \
 "/universc/test/shared/cellranger-tiny-fastq/3.0.0/tinygex_S1_L002"
```

#### Running launch_universc.sh on DropSeq data

Obtain DropSeq data from public database:

```
wget https://www.ncbi.nlm.nih.gov/geo/download/\?acc\=GSM1629192\&format\=file\&file\=GSM1629192%5FPure%5FHumanMouse%2Ebam
mv index.html\?acc=GSM1629192\&format=file\&file=GSM1629192%5FPure%5FHumanMouse%2Ebam GSM162919.bam
samtools sort -n GSM162919.bam > GSM162919.qsort
samtools view  GSM162919.qsort  HUMAN_21:9825832-48085036 > GSM162919.qsort2
samtools sort -O BAM GSM162919.bam > GSM162919.sort.bam
samtools index GSM162919.sort.bam
samtools view  GSM162919.sort.bam  HUMAN_21:9825832-48085036 > GSM162919.chr21.bam
samtools view -O BAM  GSM162919.sort.bam  HUMAN_21:9825832-48085036 > GSM162919.chr21.sort.bam
samtools sort -n GSM162919.chr21.sort.bam -o GSM162919.chr21.qsort.bam
bedtools bamtofastq -i GSM162919.chr21.qsort.bam -fq GSM1629192_chr21_R1.fastq
mv GSM1629192_chr21_R1.fastq GSM1629192_chr21_R2.fastq
fastq-dump -F --split-files SRR1873277
fastq_pair GSM1629192_chr21_R2.fastq SRR1873277_1.fastq
head -n 117060 SRR1873277_1.fastq.paired.fq 117060 > SRR1873277_1.fastq.paired.fq
head -n 117060 GSM1629192_chr21_R2.fastq.paired.fq > GSM1629192_chr21_R2.fastq.paired.fq
cp SRR1873277_1.fastq.paired.fq  GSM1629192_chr21_R2.fastq.paired.fq ~/repos/universc/test/shared/dropseq-test
cp SRR1873277_1.fastq.paired.fq  GSM1629192_chr21_R2.fastq.paired.fq ~/repos/universc/test/shared/dropseq-test
mv SRR1873277_1.fastq.paired.fq SRR1873277_R1.fastq
mv GSM1629192_chr21_R2.fastq.paired.fq  universc/test/shared/dropseq-test/SRR1873277_R2.fastq
mv GSM1629192_chr21_R2.fastq.paired.fq  universc/test/shared/dropseq-test/SRR1873277_R2.fastq
```

Run UniverSC:

```
bash universc/launch_universc.sh -t "DropSeq" --setup
# call on dropseq with files
bash universc/launch_universc.sh --id "test-dropseq" --technology "nadia" \
 --reference "universc/test/cellranger_reference/cellranger-tiny-ref/3.0.0" \
 --read1 "universc/test/shared/dropseq-test/SRR1873277_S1_L001_R1_001" \
 --read2 "universc/test/shared/dropseq-test/SRR1873277_S1_L001_R2_001" 
```

#### Running launch_universc.sh on ICELL8 data

```
# call on icell8 files with custom whitelist and non-standard file names
bash launch_universc.sh --setup -t "icell8"  --barcodefile "test/shared/icell8-test/BarcodeList.txt"
bash launch_universc.sh --id "test-icell8-custom" --technology "iCell8" \
 --reference "test/cellranger_reference/cellranger-tiny-ref/3.0.0" \
 --read1 "test/shared/icell8-test/iCELL8_01_S1_L001_R1_001.fastq" "test/shared/icell8-test/iCELL8_01_S1_L002_R1_001.fastq" \
 --read2 "test/shared/icell8-test/iCELL8_01_S1_L001_R2_001.fastq" "test/shared/icell8-test/iCELL8_01_S1_L002_R2_001.fastq" \
 --barcodefile "test/shared/icell8-test/BarcodeList.txt" \
 --jobmode "sge"
```

### Debugging

We've made considerable efforts to ensure you don't run into problems. However, it may be necessary from
time to time to troubleshoot issues calling UniverSC. For other technologies, various
changes to Cell Ranger are made in a reversible fashion. If you run into problems you can restore
Cell Ranger to default parameters:

```
bash launch_universc.sh -t "10x" --setup
```

Then you can call `launch_universc.sh` as above or configure Cell Ranger for your technology of choice such as :

```
bash launch_universc.sh --setup -t "icell8"  --barcodefile "test/shared/icell8-test/BarcodeList.txt"
```

Set up calls are particularly useful to set up the whitelist in advance of running multiple
samples simultaneously, provided they are the same technology.

It is also possible that your Cell Ranger installation will be "locked" by UniverSC.
This is intentional to prevent different technologies running simultaneously. When running
Cell Ranger, we need to ensure that the barcode whitelist corresponds to the technology that
is running and cannot be changed until existing runs will finish.

However, this means that in the case of an error or if a job is "killed", then the lock
file will not be cleared. You can do this manually as follows:

```
cellrangerversion=`cellranger count --version | head -n 2 | tail -n 1 | cut -f2 -d'(' | cut -f1 -d')'`
cellrangerpath=`which cellranger`
rm ${cellrangerpath}-cs/${cellrangerversion}/lib/python/cellranger/barcodes/.lock
```

When doing this *please ensure that no other instances are running* for Cell Ranger
convert.

You can also see the current configuration of UniverSC for each Cell Ranger
install as follows:

```
cellrangerversion=`cellranger count --version | head -n 2 | tail -n 1 | cut -f2 -d'(' | cut -f1 -d')'`
cellrangerpath=`which cellranger`
cat ${cellrangerpath}-cs/${cellrangerversion}/lib/python/cellranger/barcodes/.lastcalled
```

These columns show the barcode length, UMI length, and barcode whitelist of the last
technology used by UniverSC. Please *do not remove this file* unless the
last technology used is 10x Genomics.


## Licensing <span id="Licensing"><span>

This package is provided open-source on a GPL-3 license. This means that you are free to use and 
modify this code provided that they also contain this license.

Please note that we are third-party developers releasing it for use by users like ourselves.
We are not affiliated with 10x Genomics, Dolomite Bio, Takara Bio, or any other vendor of
single-cell technologies. This software is not supported by 10x Genomics and only changes
data formats so that other technologies can be used with the Cell Ranger pipeline.

Cell Ranger (version 2.0.2, 2.1.0, 2.1.0, and 3.0.2) has been released open source on and MIT
license on GitHub. We use this version of Cell Ranger for testing and running our tools.
Note that the code that generates the 'cloupe' files is not included in this release.
The Cloupe browser uses files generated by proprietary closed-source software and is
subject to the 10x Genomics End-User License Agreement which does not allow use with
data generated from other platforms.

Therefore 'launch_universc.sh' does not support Cloupe files and you should not use them with
technologies other than 10x Genomics.  

