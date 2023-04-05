### Manage packages with conda

Check [conda](https://docs.conda.io/en/latest/)

1)	Create a directory call `tools` under `/mnt/data`
2)	Enter directory `tools`
3)	`wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh`
4)	`bash Miniconda3-latest-Linux-x86_64.sh`
5)	`export PATH=$PATH:/home/ubuntu/miniconda3/bin`
6)	`export PATH=/home/ubuntu/miniconda3/bin:$PATH`
7)	`conda`
8)	`conda create -n bowtie2 -c bioconda bowtie2`
9)	`conda activate bowtie2`
10)	`bowtie2`
11)	`conda deactivate`
