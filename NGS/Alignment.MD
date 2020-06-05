**[Back to main page](https://yolanda-ht.github.io/BioinformaticsRandomSeed/)**

# Alignment
> Last update: 06/05/2020 <br>
> By: Huitian (Yolanda) Diao

## 1. Concept
#### 1.1 Alignment
In NGS, alignment means to compare short reads with reference genome. It generate information including the corresponding location of the reads, and quality of alignment. 
>Input: short reads (fastq format) <br>
>Output: aligned files (SAM / BAM) <br>
>Goal: Aquire abundance information of genetic features in short reads
#### 1.2 Aligner v.s. Mapper
Aligners try to find exact location of reads by base mapping, while mappers assign the reads to features without requirement of exact alignment. Mappers are usually faster that aligners.
>Aligners: Bowtie, Tophat, STAR <br>
>Mapper: Kallisto, Salmon
#### 1.3 Global v.s. local
Global alignment attemps to align the entire sequence, while local alignment trys to find regions with highest level of similarity between sequences. Local alignments are suitable for comaparing dissimilar sequences that has similar regions.
#### 1.4 Parameters
  1.4.1 Read clipping <br>
  1.4.2 Splicing <br>
  1.4.3 Insert size <br>
  1.4.4 Inner distance <br>

## 2. Algorithms
#### 2.1 Burrows-Wheeler Transformation (BWT)
BWT is a lossless data compression method, which works by rearranging character string into runs of similar characters. BWT is basis for alignment tools such as Bowtie, BWA and SOAP2.

## 3. Tools


[Single cell alignment]()

## References
1. [Wikibooks - Next Generation Sequencing(NGS) / Alignment](https://en.wikibooks.org/wiki/Next_Generation_Sequencing_(NGS)/Alignment)
2. [UC Davis Bioinformatics training](https://ucdavis-bioinformatics-training.github.io/2017-August-Variant-Analysis-Workshop/wednesday/Aligners.pdf)
3. [Bleidorn C. (2017) Alignment and Mapping. In: Phylogenomics. Springer, Cham](https://link.springer.com/chapter/10.1007/978-3-319-54064-1_6#citeas)
4. [Wikipedia - Burrows-Wheeler_transform](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform#BWT_in_bioinformatics)
