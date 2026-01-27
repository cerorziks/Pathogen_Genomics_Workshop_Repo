NGS data formats and Quality Control

              Jacqui Keane

                  @drjkeane
              drjkeane@gmail.com




 Adapted from slides provided by Petr Danecek
           petr.danecek@sanger.ac.uk
                                                1 / 48
Data Formats




               2 / 48
Data Formats



   FASTQ                                                                        Sequencing
                                                                                Instrument
     I Unaligned read sequences with base qualities
   SAM/BAM                                                                  FASTQ

     I Unaligned or aligned reads                                                 Sequence
     I Text and binary formats                                                    Alignment

   CRAM                                                                     BAM
     I Better compression than BAM
   VCF/BCF                                                                         Variant
                                                                                   Calling
     I Flexible variant call format
     I Arbitrary types of sequence variation                                VCF
     I SNPs, indels, structural variations
                                                                                  Analysis



   Specifications maintained by the Global   Alliance for Genomics and Health




                                                                                              3 / 48
FASTA - reference genome

            >1 dna:chromosome chromosome:GRCh37:1:1:249250621:1
            NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
            NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
            NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
            TATTCAAAAAATTGAGAATTTCTGACCACTTAACAAACCCACAGAAAATCCACCCGAGTG
            CACTGAGCACGCCAGAAATCAGGTGGCCTCAAAGAGCTGCTCCCACCTGAAGGAGACGCG
            CTGCTGCTGCTGTCGTCCTGCCTGGCGCCTTGGCCTACAGGGGCCGCGGTTGAGGGTGGG
            AGTGGGGGTGCACTGGCCAGCACCTCAGGAGCTGGGGGTGGTGGTGGGGGCGGTGGGGGT
            GGTGTTAGTACCCCATCTTGTAGGTCTGAAACACAAAGTGTGGGGTGTCTAGGGAAGAAG
            >2
            NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
            NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
            NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
            AAAAGCATTTATGCTACAAATTACTATGGTAATTATGCTACAAATTTATGGTACCATAAA
            TTACCATAGTAATTTGTAGCATAAATTTGTACTATGGTACAAATTACATGGGAGAGTGAA
            GGTGGGTTAAAACATTCATATTAAAGAACTTCCACTCAGATTGCAAGAAAAGAGAGAGGA
            ATGGAGATGGTAGCACAAGTCCCTACAATAAAAGTAGATGTTTTGAGATCAGTTCTATTT




                                                                           4 / 48
FASTQ

              @ERR007731.739 IL16_2979:6:1:9:1684/1           Read name
              CTTGACGACTTGAAAAATGACGAAATCACTAAAAAACGTGAAAAATGAGAAATG...   Sequence
        1
       d
              +
      a
   Re



              BBCBCBBBBBBBABBABBBBBBBABBBBBBBBBBBBBBABAAAABBBBB=@>BB...   Base qualities
              @ERR007731.740 IL16_2979:6:1:9:1419/1
              AAAAAAAAAGATGTCATCAGCACATCAGAAAAGAAGGCAACTTTAAAACTTTTC...
          2
     ad




              +
   Re




              BBABB/ABABAABABABBABBBAAA>@B@BBAA@4AAA>.>BAA@779:AAA@A...


   I      Simple format for raw unaligned sequencing reads
   I      Paired-end sequencing: two FASTQ files or one interleaved file




                                                                                           5 / 48
FASTQ

                  @ERR007731.739 IL16_2979:6:1:9:1684/1           Read name
                  CTTGACGACTTGAAAAATGACGAAATCACTAAAAAACGTGAAAAATGAGAAATG...             Sequence
        1
       d
                  +
      a
   Re



                  BBCBCBBBBBBBABBABBBBBBBABBBBBBBBBBBBBBABAAAABBBBB=@>BB...             Base qualities
                  @ERR007731.740 IL16_2979:6:1:9:1419/1
                  AAAAAAAAAGATGTCATCAGCACATCAGAAAAGAAGGCAACTTTAAAACTTTTC...
          2
     ad




                  +
   Re




                  BBABB/ABABAABABABBABBBAAA>@B@BBAA@4AAA>.>BAA@779:AAA@A...


   I      Simple format for raw unaligned sequencing reads
   I      Paired-end sequencing: two FASTQ files or one interleaved file

   I      Quality encoded in ASCII characters with decimal                    codes 33-126
              I    ASCII code of “A” is 65, the corresponding quality is Q = 65 − 33 = 32

                     Base quality encoded as character
                            ! " # $ % & ' ( ) * + , - . / 0 1 2 3 4 5 6 7 8 9 : ; < = > ? @ A B C D E F G H I J

                     Numeric ASCII value
                           33 . . . . . . . . . . . .    47 . . . . . . . . . . . . . . . . .   65 . . . . . . . .

                     Base quality value                                                            (65-33 = 32)
                            0 . . . . . . . . . . . .    14 . . . . . . . . . . . . . . . . .   32 . . . . . . . .




                                                                                                                     6 / 48
Quality = Phred-scaled probability of an error



                   Quality    Probability of error   Accuracy
                   10 (Q10)   1 in 10                90%
                   20 (Q20)   1 in 100               99%
                   30 (Q30)   1 in 1000              99.9%
                   40 (Q40)   1 in 10000             99.99%




                 Q = −10 log10 P       ...       P = 10−Q/ 10




                                                                7 / 48
SAM / BAM: Sequence Alignment/Map format




                                           8 / 48
SAM / BAM: Sequence Alignment/Map format




   Flag
       Hex     Dec     Flag                Description
       0x1     1       PAIRED              paired-end (or multiple-segment) sequencing technology
       0x2     2       PROPER_PAIR         each segment properly aligned according to the aligner
       0x4     4       UNMAP               segment unmapped
       0x8     8       MUNMAP              next segment in the template unmapped
       0x10    16      REVERSE             SEQ is reverse complemented
       0x20    32      MREVERSE            SEQ of the next segment in the template is reversed
       0x40    64      READ1               the first segment in the template
       0x80    128     READ2               the last segment in the template
       0x100   256     SECONDARY           secondary alignment
       0x200   512     QCFAIL              not passing quality controls
       0x400   1024    DUP                 PCR or optical duplicate
       0x800   2048    SUPPLEMENTARY       supplementary alignment


   Bit operations made easy
     - samtools flags
        0xa3 163 PAIRED,PROPER_PAIR,MREVERSE,READ2
     - python
        0x1 | 0x2 | 0x20 | 0x80 .. 163
        bin(163) .. 10100011




                                                                                                    9 / 48
SAM / BAM: Sequence Alignment/Map format




   Insert size
   length of the DNA fragment sequenced from both ends by paired-end sequencing:




                                                                                   10 / 48
CRAM: Reference based Compression
   BAM files are too large
     I   ~1.5-2 bytes per base pair

   Increases in disk capacity are being far outstripped by sequencing technologies




         Zachary D. Stephens, et al, Big Data: Astronomical or Genomical? DOI: 10.1371/journal.pbio.1002195




                                                                                                              11 / 48
CRAM: Reference based Compression
   BAM files are too large
     I   ~1.5-2 bytes per base pair

   Increases in disk capacity are being far outstripped by sequencing technologies
   BAM stores all of the data
     I   Every read base
     I   Every base quality
     I   Using a single conventional compression technique for all types of data

                    Reference sequence: ACGTACGTACGTACGTACGTACGTACGTACGTAC
                    read 1:             ACGTACGTACGTACGTACGTGC
                    read 2:                TACGTACGCACGTACGTGCGTA
                    read 3:                  CGTACGCACGTACGTACGTACG
                    read 4:                    TACGTACGTACGTGCGTACGTA
                    read 5:                      CGCACGTACGTACGTACGTACG
                    read 6:                            TACGTGCGTACGTACGTAC




                                                                                     12 / 48
CRAM: Reference based Compression
   BAM files are too large
     I   ~1.5-2 bytes per base pair

   Increases in disk capacity are being far outstripped by sequencing technologies
   BAM stores all of the data
     I   Every read base
     I   Every base quality
     I   Using a single conventional compression technique for all types of data

                    Reference sequence: ACGTACGTACGTACGTACGTACGTACGTACGTAC
                    read 1:             ....................G.
                    read 2:                ........C.............
                    read 3:                  ......C...............
                    read 4:                    .............G........
                    read 5:                      ..C...................
                    read 6:                            .....G.............

   CRAM: in lossless mode 60% of BAM size
     I   Reference based compression
     I   Controlled loss of quality information
     I   Different compression methods for different type of data




                                                                                     13 / 48
VCF: Variant CallFormat




   File format for storing variation data
     I   tab-delimited text, parsable by standard UNIX commands
     I   flexible and user-extensible
     I   compressed with BGZF (bgzip), indexed with TBI or CSI (tabix)




                                                                         14 / 48
VCF anatomy




     Row-oriented, tab-delimited file with eight mandatory columns   (CHROM-INFO)




                                                                                    15 / 48
VCF anatomy




              Genomic coordinates




                                    16 / 48
VCF anatomy




              Arbitrary string, typically a dbSNP RefSNP id.   Dot for
                                     missing value.




                                                                         17 / 48
VCF anatomy




              Reference sequence - chr1




                                          A   654,321




                                          T
                                          C   1,234,567



                                          C   1,456,789




                                                          18 / 48
VCF anatomy




              Reference sequence - chr1




                                          A   654,321     AA   A




                                          T
                                          C   1,234,567   G    G



                                          C   1,456,789   C    T




                                                                   19 / 48
VCF anatomy




              Although in theory phred-scaled probability, don’t expect
                    truly probabilistic interpretation in practice.




                                                                          20 / 48
VCF anatomy




              Soft-filter variants with e.g. low quality, low depth, etc.




                                                                            21 / 48
VCF anatomy




              Per-site annotations. Here DP is the cumulative read depth
               across all samples and AF allele frequency of the allele in
                                   general population.




                                                                             22 / 48
VCF vs BCF

   VCFs can be very big
    I  compressed VCF with 3781 samples, human data:
           I   54 GB for chromosome 1
           I   680 GB whole genome
   VCFs can be slow to parse
    I  text conversion is slow
    I  main bottleneck: FORMAT fields




   BCF
    I    binary representation of VCF
    I    fields rearranged for fast access




                                                       26 / 48
File formats summary




                       27 / 48
File formats summary




                       28 / 48
