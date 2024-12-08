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

