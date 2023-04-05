### Sequence file formats
#### fasta
  The FASTA file format is the simplest way of representing nucleic acid of protein sequences using single-letter codes for nucleotides or amino acids.
  For each sequence, there are two lines: 
  - The first is a sequence identifier, which contains information about the sequence, preceded with a “>” symbol. If you retrieve a sequence from GenBank, SWISS-PROT, BLAS, or another database, the identifier will follow a standardized format. 
  - The second line in a FASTA file is the nucleotide or amino acid sequence, using single letter IUPAC codes (etc, ATCG).
  
  File extension: `.fa`, `.fasta`, `.faa`, `.fas`, etc.
```
>Chr01
TTAGGGTTTACGAAGAAATTTGGGTTTTTGATCTTTGAACACAAAATTAAGGCATTTAGAGGTGTTTTAGGGTTTAGGGT
TTAGGGTTTGAGGTTGGGGTTTGGGTTTTAGGTTTTAGGATTTAGGTTTTACGATTTAGGGTTTATGGTTTATGGTTTAT
GGTTTACGATTTAGGTTTTTGGTTTAGGGTTTAGGGTTTTGGGTTTAGGGTTTAGGAAATAATTTGGGTCTTTCATCTTT
CAACACAAAATGAAGGGATTTAGAGGCATTTTTAGGGTTTAGGGTTTAAGGTTTCGGGTTTGGGTTTTAGATTTTACTGT
TTACGATTTACGGTTTAGGGTTTAGGGTTTTAGGTTTTAGGTTTTGGGTTTGGGTTTTAGGGTTTATAATGTTGGGTTTA
GGGTTTACGGTTTATAGTTTAGGGTTTACCAAGAAATTTCGGTGTTTCCTATTCGAACACAAAAGTAAGGCAGTTACTGA
```
#### fastq
  The FASTQ format was developed for and used with next-generation sequencing instruments and builds off of the simplicity of the FASTA format. Information about the quality (“Q” in “FASTQ” stands for quality) of the sequencing reads and base calls are a defining component of the FASTQ file format.
  For each sequence within a FASTQ file, there are four lines:
  - The first is a sequence identifier and description. It begins with an “@” symbol followed by information about the sequence. There is a standardized format with Illumina sequencers that includes the unique instrument name, the flowcell lane, etc.
  - The second line contains the raw sequence data as with a FASTA file
  - The third line includes the “+” symbol along with a repeated identifier
  - The fourth line is the quality score for each base in the sequence on the second line and must be the same length.
  Check Phred score [here](https://en.wikipedia.org/wiki/Phred_quality_score)
```
@A00599:307:HMVHVDSX3:1:1101:8594:1000 1:N:0:ATCACGTG+GTCTCATG
CTCCTCGTAGCCTTTGGTGAAGTAGAGCATGGCTTTCGCATATCTCTCTGGGGTCTCCCGCAAACCTTCTCTTTCTGGATCCTCTCCAATGCACTCCAGAATGGTTCTCACTGCACCTGCCAATTTTTGAACTCGTTCCTCCGTTTCCTC
+
FFFFFFFFFFFFFFFFFFFFFFFFFFF:FFFFFFFFFFFFFFFFFFFFFFFFFFFFF:FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF:FFFFFFFFFFFFFF:FFFFFF:FFFFFFFFFFFFFFFFF:FF
@A00599:307:HMVHVDSX3:1:1101:15157:1000 1:N:0:ATCACGTG+GTCTCATG
GCGGGTCCAGTGTATGGGGCAGCAACAGCCGAGAATCCAAGGCAGTCTCTGACGTTGCCGGTGGGCACGGTGGCAGTGTTGGAGGCAGCAAACACCTGCCACTTGGGGTTACCGGGCACGATGGTGCTGTTGGTGGTGGGGCAGGCCATG
+
FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF:FFFFFFFF,FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF:FFFFF:FF,FFFFFFFFFFFFFFFFFFF
```
### Alignment file formats
- #### sam and bam
  Check [here](https://samtools.github.io/hts-specs/)
  
- #### paf
  Check [here](https://lh3.github.io/minimap2/minimap2.html#10)

### Generic feature formats
- #### gff, gtf
  Check [here](https://asia.ensembl.org/info/website/upload/gff.html)
  
- #### gff3
  Check [here](https://asia.ensembl.org/info/website/upload/gff3.html)

```
##gff-version 3
##annot-version TAIR10
Chr1    phytozomev10    gene    3631    5899    .       +       .       ID=AT1G01010.TAIR10;Name=AT1G01010
Chr1    phytozomev10    mRNA    3631    5899    .       +       .       ID=AT1G01010.1.TAIR10;Name=AT1G01010.1;pacid=19656964;longest=1;Parent=AT1G01010.TAIR10
Chr1    phytozomev10    exon    3631    3913    .       +       .       ID=AT1G01010.1.TAIR10.exon.1;Parent=AT1G01010.1.TAIR10;pacid=19656964
Chr1    phytozomev10    five_prime_UTR  3631    3759    .       +       .       ID=AT1G01010.1.TAIR10.five_prime_UTR.1;Parent=AT1G01010.1.TAIR10;pacid=19656964
Chr1    phytozomev10    CDS     3760    3913    .       +       0       ID=AT1G01010.1.TAIR10.CDS.1;Parent=AT1G01010.1.TAIR10;pacid=19656964
Chr1    phytozomev10    exon    3996    4276    .       +       .       ID=AT1G01010.1.TAIR10.exon.2;Parent=AT1G01010.1.TAIR10;pacid=19656964
Chr1    phytozomev10    CDS     3996    4276    .       +       2       ID=AT1G01010.1.TAIR10.CDS.2;Parent=AT1G01010.1.TAIR10;pacid=19656964
Chr1    phytozomev10    exon    4486    4605    .       +       .       ID=AT1G01010.1.TAIR10.exon.3;Parent=AT1G01010.1.TAIR10;pacid=19656964
```
### Something more
- #### vcf and bed
  Check [here](https://samtools.github.io/hts-specs/)
  
- #### and more glossary
  Check [here](https://asia.ensembl.org/info/website/glossary.html)
