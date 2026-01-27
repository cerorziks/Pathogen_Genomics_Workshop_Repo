Illumina Sequencing
     Technology
    Michael Quail
   mq1@sanger.ac.uk
               Solexa
» Launched their Genome Analyzer in 2006
» Spinout from Cambridge University, set up
  at Gt. Chesterford in 2000
» At launch GA gave 1Gb/run. Now upto 9Tb.
» Acquired by Illumina in 2007
» Short read sequencing
» Accurate (0.2-0.4% error)
» Market leader.
» $2-$50/Gb
   Illumina workflow
 DNA Prep




Library Prep




 Clustering




Sequencing       Analysis
                            Illumina Paired End
5’
                                Library Prep
                        P


          T                 5’                         A
          P
                    +       A                          5’
                                                            P



3’                                       T4 DNA Ligase
                                                                                     R1 sequencing primer

              5’                                                      3’


                                 T                       A
                                                         T
                             A

                                                                                     Reverse compliment of R2 primer
                                                                      5’
              3’

                   P5                    Hybridize primers


              5’                                                      3’   P7


                             T                           A
                                                         T
                             A


                                                                      5’
              3’
                                         Limited PCR



              P5                                                           P7
     5’                              T                      A                   3’
     3’                              A                      T                   5’

                                         Make clusters and sequence
      Illumina Library Insert sizes
          Exome, targeted, ChiP, ATAC
     P5               SP 1          100-200bp


                                                 SP2                         P7
                      Primer site
                                                 Primer site

Reads need to be just long enough to map and ideally not to overlap exon boundaries




    Whole Genome
     P5               SP 1           400-600bp                                    P7


                                                               SP2
                      Primer site
                                                               Primer site

    Fragments need to be just long to span common repeat elements eg AluI
    with unique sequence on either side so can map
Illumina Truseq Library Prep
       Dual indexing
         i5

          i7



        i5             i7
         i7       i5
Illumina workflow
 DNA Prep




Library Prep




 Clustering




Sequencing     Analysis
                     3’         Cluster Amplification




// ///////////////        ///       //// ////////////////   ////
      SURFACE                                SURFACE



  Single-molecule                             Cluster                 1.5 Billion
       array                                  ~1000                  clusters on a
                                             molecules             single glass chip
Illumina Sequencing methodology
Illumina Sequencing methodology




Millions of these single library fragments are bound at random to the flowcell surface
Illumina Sequencing methodology




    That strand is copied by a DNA polymerase from the primer grafted on the flowcell surface,
    this duplex is then denatured and the original strand washed away
Illumina Sequencing methodology
Illumina Sequencing methodology




                    That strand can be copied
   Illumina Sequencing methodology




After denaturation you then have two strands bound to
the grafted primer lawn.
Illumina Sequencing methodology




          Which can loop over and be copied
Illumina Sequencing methodology




              And so on to form clusters of around 1000
              copies of the original fragment
                                Preparing Clusters for
                                  Sequencing read 1
                                                                  3’                              3’




3’                                3’


     / ////////////////   ///          / ////////////////   ///        // ///////////////   ///        / ////////////////   ///
           SURFACE                           SURFACE                         SURFACE                         SURFACE



     CLUSTERS                     LINEARISATION                         BLOCKING                   SEQ. PRIMER
                                                                                                  HYBRIDISATION
iSeq100, HiSeq4000, Xten, NovaSeq
Illumina workflow
 DNA Prep




Library Prep




 Clustering




Sequencing     Analysis
Sequencing by Synthesis

         » Extend by 1 base

         » Image


         » Reverse
           termination


         » Repeat
          Illumina Modified Nucleotides
                                 PPP        5’       Base
                 Natural dNTP:                   O




                                       3’   OH




Reversible florescent dTTP:
Two Channel SBS – NextSeq, MiniSeq and NovaSeq
                             Error

» Sequence quality Q is reported on a log scale
» Q10 is 1 error in 10
» Q20 is 1 error in 100
» Q30 is 1 error in 1000
» Q40 is 1 error in 10000
» Q50 is 1 error in 100000
Error limits read length
     Illumina sequencing
         with indexing
With Illumina sequencing you sequence the insert from
   each end. And youc an also perform sequencing
 reactions that read the sequence of the index in the
        introduced adapter. So how is this done
Dual indexing method B

         Also NovaSeq on v1.5 onwards
Dual indexing method A
Each cluster contains many strands extended
from the grafted P7 flowcell primer.
The first sequencing primer is annealed and this sits immediately
upstream of the DNA insert. The first base sequenced is the first
base of the insert
The instrument does the first read
Then that strand is dissociated and washed away and another primer
annealed just upstream of the i7 adapter index so it can be sequenced
That strand is dissociated and washed away and the 3’ ends of
the P5 oligos on the flowcell surface deblocked.
Then the sequence of the i5 ndex read
Synthesis is allowed to carry on to form the complement strand
Reagents are added that cleave the original strand. A read
2 primer is anneal to the P7 end this time
The sequence from the other end of the insert is obtained
Instruments
Economics of Illumina ’s Sequencing Portfolio


Platform       Flow Cell   $/G                              $/G
                           (300 CYC.)
                                                          (300 CYC.)


               10B         $3
Novaseq X/X+
               25B         $2

               S4          $5
NovaSeq 6000
               SP          $15.40


NextSeq 2000   P3          $20.00


NextSeq
               P2          $29.50
1000/2000


NextSeq 550    HO          $41.38



NextSeq 550    MO          $47.50



MiSeq          v2          $236.00


                                        $0   $50   $100       $150     $200
Novaseq X – 2023 launch
        $1.25M
    $3/Gb on 10 B flowcell
    $2/Gb on 25 B flowcell




           10B 2x150 in 24 hours
           25B 2x150 in 48 hours
NovaseqX+

            •   2 x 8-lane flow cells
            •   High resolution optics allow
                for tighter spacing of
                nanowells on flow cell
                surface enabling higher
                read counts vs. NS6000.
            •   New X-LEAP-SBS
                chemistry with improved
                reagent stability
            •   Faster incorporation times
            •   Improved sustainability of
                reagent supply
            •   Novaseq X and X+ are
                integrated with DRAGEN
                Bio-IT Platform
       A Closer Look At 1-Dye Chemistry
       Cluster Generation and SBS

                                                        What’s the Same?



                     Library Preparation                   Cluster Growth                  Sequencing




                                   The iSeq™ 100 System still utilizes the Illumina SBS chemistry,
                                               where each base is added one at a time



     79

CONFIDENTIAL – FOR INTERNAL USE ONLY
       A Closer Look At 1-Dye Chemistry
       Cluster Generation and SBS

                                             What’s the Different?




                                                                          Nucleotides are

            A G T C                                                       labeled with a single
                                                                          dye, with the exception
                                                                          of the G nucleotide

          Cleavable                    No    Fixed      Dye added
             dye                       dye    dye    post-incorporation




     80

CONFIDENTIAL – FOR INTERNAL USE ONLY
       A Closer Look At 1-Dye Chemistry
       SBS and Imaging

                                           Sequencing by Synthesis



                                               Sequencing Cycle



                    A      + T
                                                             A        A
                    C
                    T
                    G
                    G
                                                             C        C
                  Incorporation           Imaging              Chemistry              Imaging



                   An intermediate chemistry step, which removes the dye from the A nucleotide
                           and adds a dye to the C nucleotide, separates the two images



     81

CONFIDENTIAL – FOR INTERNAL USE ONLY
       A Closer Look At 1-Dye Chemistry
       SBS and Imaging

                                       Imaging




                    A G T C                      Using the two images, the
                                                 iSeq™ 100 innovative data
                                                 processing approach
          Image 1




                                                 uniquely determines
                                                 which nucleotide was
                                                 added to the growing
          Image 2




                                                 template strand




                    A G T C
     82

CONFIDENTIAL – FOR INTERNAL USE ONLY
                 MiniSeq


» Single lane, 2x 150 reads, upto 7.5Gb
» Two output modes 8M or 25 M reads
» Less than 24 hour run time
» Cheapest Illumina sequencer $49.5K
» Runs from $500 to $1500
» 2 Colour chemistry
                    Illumina MiSeq

» Single-lane version of HiSeq
» Read length: 2 x 300 (1 -2 days)
» Error rate 0.1%
» Yield: > 10 Gb / run
» $99,000 capital cost
» $100-$240 / Gb
                    Illumina MiSeq

» Single-lane version of HiSeq
» Read length: 2 x 300 (1 -2 days)
» Error rate 0.1%
» Yield: > 10 Gb / run
» $99,000 capital cost
» $236 / Gb
MiSeq i100

             • Faster. 7.5hr run for 2 x 150
             • 40% cheaper than Miseq
             • Does Index read first.
             • Better with low complexity?
             • 5% phiX for 16S
             • RT reagents
             • Patterned flowcell
             • 2 x 500 coming
              Illumina NextSeq 500

» Uses only 2 dyes / 2 images not 4
» Read length: 2 x 150 (1.25 days)
» Yield: 120 Gb / run
» $250,000 capital cost
» $30-$45 / Gb
NextSeq 1000/2000
NextSeq 1000: $210k
NextSeq 2000: £335k

     £20-$30/Gb
        Hiseq 3000/4000
» Single or double flowcell instrument
» Suitable for all applications inc. exomes
» Patterned flowcell (aka “PFCT”)
» $24/Gb ($20/Gb at launch)


                                     Defined feature
                                     Ordered spacing
HiSeq Flowcell Tray
                   Illumina HiSeq X

» Ultra-high throughput
» Read length: 2x150 (3 days)
» Yield: 1.6 Tb / run
» $1,000,000 capital cost x 10
» $ 8/Gb (7 at launch)
» The $1000 Genome
2017: NovaSeq
Economics of Illumina ’s Sequencing Portfolio


Platform       Flow Cell   $/G                              $/G
                           (300 CYC.)
                                                          (300 CYC.)

               S4          $6
NovaSeq 6000   SP          $15.40



NextSeq 2000   P3          $20.00


NextSeq
               P2          $29.50
1000/2000


NextSeq 550    HO          $41.38



NextSeq 550    MO          $47.50



MiSeq          v2          $236.00


                                        $0   $50   $100        $150    $200
Sequencing kits
NovaseqX


      £3/Gb   £2/Gb
Novaseq 6000 Kits
          Cost per Gb depends on Kit used


                                                               Max
                                                               Output      Max
                                                      Number per flow      Output     Total Price Price per     Price per
                  Instrument     Cycle Kit   Cycles
                                                      of Lanes cell (Gb)   per lane   per Flow Cell lane        max Gb
                                                               [Illumina   (Gb)
                                                               Spec]
 1   HiSeq 4000                       2x25     50         8         125     15.625     $9,640.00    $1,205.00      $77.12
 2   HiSeq 4000                       2x50    100         8         250     31.25     $12,747.50    $1,593.44      $50.99
 3   HiSeq 4000                      2x75     150         8         375     46.875    $13,135.00    $1,641.88      $35.03
 4   HiSeq 4000                      2x150    300         8         750     93.75     $18,480.00    $2,310.00      $24.64
 5   HiSeq X10                       2x150    300        16        1800     112.5     $14,348.00      $896.75       $7.97
 6   NovaSeq SP                       2x50    100         1          80       80       $2,250.00    $2,250.00      $28.13
 7   NovaSeq SP                      2x150    300         1         250      250       $3,850.00    $3,850.00      $15.40
 8   NovaSeq SP                      2x250    500         1         400      400       $5,500.00    $5,500.00      $13.75
 9   NovaSeq S1                       2x50    100         1         167      167       $4,100.00    $4,100.00      $24.55
10   NovaSeq S1                      2x100    200         1         333      333       $5,500.00    $5,500.00      $16.52
11   NovaSeq S1                      2x150    300         1         500      500       $6,600.00    $6,600.00      $13.20
12   NovaSeq S2                       2x50    100         1         417      417       $9,500.00    $9,500.00      $22.78
13   NovaSeq S2                      2x100    200         1         833      833      $13,000.00   $13,000.00      $15.61
14   NovaSeq S2                      2x150    300         1        1250      1250     $15,250.00   $15,250.00      $12.20
15   NovaSeq S4                      2x100    200         1        2000      2000      ~$20000      ~$20000          ~$10
16   NovaSeq S4                      2x150    300         1        3000      3000      ~$21000      ~$21000           ~$7
                    Your text here
Illumina workflow
 DNA Prep




Library Prep




 Chip Prep




Sequencing     Analysis
          The Software Challenge

» Analysis pipeline (images -> sequence)
» Tracking of projects, samples, runs + analysis
» Data storage
» QC (manual + automatic)
» Sequence alignment + assembly
» Variant calling
» Interpretation
             Costs
» 1st human genome:
  ~ $500 Million
» Current capillary cost :
  ~ $10 Million
» Illumina cost:
  ~ $1,000 on Xten
  ~$500 on Novaseq 6000
  ~$200-300 on Novaseq X
    Limitations of Illumina
    Sequencing Technology
» Some systematic errors
  » Difficult to spot rare variants (<1%)
» Low complexity templates
» Sequencing short fragments doesn’t give
  any long range information
» Index Hopping
     Limitations of Illumina
     Sequencing Technology
» Some systematic errors
  » Difficult to spot rare variants (<1%)
  » See Duplex seq by Schmitt et al.,
  » Nanoseq https://doi.org/10.1038/s41586-021-
    03477-4
» Low complexity templates
» Sequencing short fragments doesn’t give any
  long range information
» Index Hopping
    Limitations of Illumina
    Sequencing Technology
» Some systematic errors
  » Difficult to spot rare variants (<1%)
» Low complexity templates
  » Add complex library to 30%, phase, ensure
    variation at start of read
» Sequencing short fragments doesn’t give
  any long range information
» Index Hopping
Low quality 16S run
    Limitations of Illumina
    Sequencing Technology
» Some systematic errors
  » Difficult to spot rare variants (<1%)
» Low complexity templates
» Sequencing short fragments doesn’t give
  any long range information
  » Use long range sample prep method
» Index Hopping
       Illumina long range
           approaches
» 10 x Genomics
» HiC (eg Arima and Dovetail)

» Tell-Seq
» Haplotagging (Meier et al., BioRxIV
  2020                   )
       doi: https://doi.org/10.1101/2020.05.25.113688


» Constellation
    Limitations of Illumina
    Sequencing Technology
» Some systematic errors
  » Difficult to spot rare variants (<1%)
» Low complexity templates
» Sequencing short fragments doesn’t give
  any long range information
» Index Hopping
        Limitations of Illumina
        Sequencing Technology
» Index Hopping




See Sinha et al BioRXIV 2017. http://biorxiv.org/content/early/2017/04/09/125724
Any Questions ?

   mq1@sanger.ac.uk
