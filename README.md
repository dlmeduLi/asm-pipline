# asm-pipeline

## Usage

> asm-pipeline genome.asm.config input.bam

## Config file

```bash

# ref genome: ref.fa
# all chroms in one file
# You can use this cmd to get this file : cat mm9/chr[0-9XYM]+.fa > mm9.ref.fa
ref_fa=mm9.ref.fa

# genome type : mm9
# supported type : mm9, mm10, hg18, hg19
# if this opttion is not setted, you must set correct value for genome_library and genome_name
genome_type=mm9

# Bioconductor BSgenome library name: BSgenome.Mmusculus.UCSC.mm9
# genome_library=BSgenome.Hsapiens.UCSC.hg19
# genome_library=BSgenome.Mmusculus.UCSC.mm9

# genome library object name : Mmusculus Hsapiens Scerevisiae
# genome_name=Hsapiens
# genome_name=Mmusculus

###################################
# Tagmeth & ASM related paramters #
###################################

# used to genereate methylated & unmethylated tagmeth index
unmeth_score=0.2
meth_score=0.8

# sliding window size, asm size,  methylated & unmethylated indexes for asm
sw_size=50
asm_size=500
meth_index=5
unmeth_index=5
```
