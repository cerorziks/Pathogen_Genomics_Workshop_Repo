NGS data formats and Quality Control

              Jacqui Keane

                  @drjkeane
              drjkeane@gmail.com




 Adapted from slides provided by Petr Danecek
           petr.danecek@sanger.ac.uk
                                                1 / 48
Quality Control




                  29 / 48
Quality Control




    The commands I run:
        samtools stats file.bam > file.bam.stats
        plot-bamstats -p plots/ file.bam.stats



    The questions I want to answer:
     I  Do I have enough read coverage with my reads?
     I  Was the library creation process efficient and problem-free?
     I  Did the sequencing process create artefacts?




                                                                       30 / 48
Read coverage



   Read coverage / depth
     I   is every genomic position “covered” to a sufficient depth?
     I   maximum average depth: (number-of-reads x read-length) / target-size
     I   average depth: (number-of-reads-mapped x read-length) / target-size
           I   the whole bacteria genome   target-size = reference sequence length = 4Mbp




   Useful coverage
     I  10x ok for variants calling
     I  30x ok for most things (variant calling, assembly)
     I  100x more than enough, pipelines subsample down to this


                                                                                            31 / 48
Library prep biases: PCR duplicates

    Experiments start with small amounts of DNA
      I a PCR amplification step is necessary for Illumina sequencing:    one molecule =>
        many identical molecules
    Problem:
      I additional PCR-copy molecules are not informative
    Solution:
      I  infer and mark PCR-dupliates, discount in later analysis
           I   mark if reads and their mates start at the same position
      I   use picard MarkDuplicates or samtools markdup
      I   typical dup rates: Exomes ~ 15-20%, Genomes < 5%




                                                                                            32 / 48
Base quality

    Sequencing by synthesis: dephasing
      I growing sequences in a cluster gradually desynchronize
      I error rate increases with read length

    Calculate the average quality at each position across all       reads




                             Quality    Probability of error   Call Accuracy
                             10 (Q10)   1 in 10                90%
                             20 (Q20)   1 in 100               99%
                             30 (Q30)   1 in 1000              99.9%
                             40 (Q40)   1 in 10000             99.99%


                                                                               33 / 48
Base quality




               34 / 48
Base quality




               35 / 48
GC bias


   GC- and AT-rich regions are more difficult to amplify
    I  compare the GC content against the expected distribution (reference sequence)




                                                                                       36 / 48
GC bias


   GC- and AT-rich regions are more difficult to amplify
    I  compare the GC content against the expected distribution (reference sequence)




                                                                                       37 / 48
GC bias


   GC- and AT-rich regions are more difficult to amplify
    I  compare the GC content against the expected distribution (reference sequence)




                                                                                       38 / 48
GC content vs depth




                      39 / 48
GC content vs depth




                      40 / 48
GC content by cycle



   Was the adapter sequence trimmed?




                                       41 / 48
GC content by cycle



   Was the adapter sequence trimmed?




                                       42 / 48
Fragment size

   Paired-end sequencing: the size of DNA fragments matters




                                                              43 / 48
Fragment size

   Paired-end sequencing: the size of DNA fragments matters




                                                              44 / 48
Quality Control



    FastQC/MultiQC are alternative tools for QC
        fastqc *.fastq.gz
        multiqc .




                                                  45 / 48
Quality Control




    Other tools I use:
       kraken - a taxonomic classification tool for sequence data
       bactinspector - determines the most probable species based on sequence data
       confindr - detection of intraspecies and cross-species
                       contamination in bacterial whole-genome sequence data

    Other important questions I ask
      I Is my sequence data the species I think it is?
      I Is there any contamination in my samples?
            I Intraspecies contamination e.g. heterozygous SNPs

            I Cross-species contamination e.g. GC content, bactinspector/confindr




                                                                                    46 / 48
