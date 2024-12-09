# BioEC131-FinalProject
COVID Variants Genome Analysis Data Package

## 1. Install jBrowse
Follow the instructions on https://currentprotocols.onlinelibrary.wiley.com/doi/10.1002/cpz1.1120 to install jbrowse.

## 2. Download the necessary COVID Variant files for analysis
In order to download the FASTA and GFF3 files, we will be fetching the NCBI data using their EDirect tools. Depending on your system, follow the instructions below to install Entrez Direct Tools:

For Linux/Unix/macOS:
```
sudo apt update
sudo apt install -y perl wget
```

For macOS, use Homebrew:
```
brew install perl wget
```

Install EDirect Tools
```
cd ~
wget https://ftp.ncbi.nlm.nih.gov/entrez/entrezdirect/edirect.tar.gz
tar -xzf edirect.tar.gz
rm edirect.tar.gz
export PATH=$PATH:$HOME/edirect
```

Access your shell configuration file ```nano ~/.zshrc``` for Zsh or ```nano ~/.bashrc``` for Bash
and add the following line to the file, save, and exit
```
export PATH=$PATH:$HOME/edirect
```
Then, enter ```source ~/.zshrc``` or ```source ~/.bashrc``` to reload your shell config file.


Now, you can use the following commands to fetch the 5 FASTA files and 5 GFF3 files for the COVID Variants. 
```
efetch -db nucleotide -format fasta -id OQ204161 > Alpha.fasta
efetch -db nucleotide -format gff -id OQ204161 > Alpha.gff
efetch -db nucleotide -format fasta -id OL678795 > Beta.fasta
efetch -db nucleotide -format gff -id OL678795 > Beta.gff
efetch -db nucleotide -format fasta -id OL852672 > Gamma.fasta
efetch -db nucleotide -format gff -id OL852672 > Gamma.gff
efetch -db nucleotide -format fasta -id OL873994 > Delta.fasta
efetch -db nucleotide -format gff -id OL873994 > Delta.gff
efetch -db nucleotide -format fasta -id OL845686 > Omicron.fasta
efetch -db nucleotide -format gff -id OL845686 > Omicron.gff
```
