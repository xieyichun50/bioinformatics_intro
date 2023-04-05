### Sequence file formats
#### fasta
  The FASTA file format is the simplest way of representing nucleic acid of protein sequences using single-letter codes for nucleotides or amino acids.
  For each sequence, there are two lines: 
  - The first is a sequence identifier, which contains information about the sequence, preceded with a “>” symbol. If you retrieve a sequence from GenBank, SWISS-PROT, BLAS, or another database, the identifier will follow a standardized format. 
  - The second line in a FASTA file is the nucleotide or amino acid sequence, using single letter IUPAC codes (etc, ATCG).
  
  File extension: `.fa`, `.fasta`, `.faa`, `.fas`, etc.

#### fastq
  The FASTQ format was developed for and used with next-generation sequencing instruments and builds off of the simplicity of the FASTA format. Information about the quality (“Q” in “FASTQ” stands for quality) of the sequencing reads and base calls are a defining component of the FASTQ file format.
  For each sequence within a FASTQ file, there are four lines:
  - The first is a sequence identifier and description. It begins with an “@” symbol followed by information about the sequence. There is a standardized format with Illumina sequencers that includes the unique instrument name, the flowcell lane, etc.
  - The second line contains the raw sequence data as with a FASTA file
  - The third line includes the “+” symbol along with a repeated identifier
  - The fourth line is the quality score for each base in the sequence on the second line and must be the same length
  Check Phred score [here](https://en.wikipedia.org/wiki/Phred_quality_score)
  
### Alignment file formats
- #### sam, bam, vcf, bed
  Check [here](https://samtools.github.io/hts-specs/)
- #### paf
  Check [here](https://lh3.github.io/minimap2/minimap2.html#10)

### Generic feature formats
- #### gff, gtf
  Check [here](https://asia.ensembl.org/info/website/upload/gff.html)
- #### gff3
  Check [here](https://asia.ensembl.org/info/website/upload/gff3.html)

### Something more
- #### vcf and bed
  Check [here](https://samtools.github.io/hts-specs/)
- #### and more glossary
  Check [here](https://asia.ensembl.org/info/website/glossary.html)
