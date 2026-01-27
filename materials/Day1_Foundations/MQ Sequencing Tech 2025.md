Sequencing Technologies

       Michael Quail
       mq1@sanger.ac.uk
                Short Read
                Sequencers
                                              Illumina
                                              Nextseq

Omniome




          Element   Ultima UG100
                                   Singular
                                   S4
                   Long Read Sequencers


                                  Oxford Nanopore P48

    PacBio Revio
                                                                     Oxford Nanopore gridION




                                            Oxford Nanopore minION

                    PacBio Vega



Generate much longer reads that enable more of the genome to be covered
Generally more expensive than short read, with higher input requirements,
Single molecule so yields dependent on DNA quality
Sanger Sequencing
         Frederick Sanger

» Discovered DNA sequencing by chain
  termination method
» Nobel Prize 1 (1958)
  » Complete amino acid
    sequence of insulin
» Nobel Prize 2 (1980)
  » For DNA sequencing
                   Primer Extension
                             DNA Polymerase


           Primer

               dATP
               dGTP
               dCTP
               dGTP

               Nucleotides       NEW
                                 STRAND




Template DNA
                Dideoxy Nucleotides


• Lack an -OH group at the 3-
    carbon position
•   Cannot add another
    nucleoside at that position
•   Prevent further DNA
    synthesis
All Possible Terminations
 Original Sanger Sequencing
» 4 sequencing reactions performed for each
  template, each with different terminator
» Radioactive primer or nucleotide used
» Sequencing reactions run on <1mm
  polyacrylamide gel cast between two glass
  plates to separate fragments according to
  size
» After run gel exposed to film and
  developed to reveal image
Sequencing gel autorad
Fluorescent Terminators
Fluorescent Gel Sequencing
ABI Capillary 3730
DNA Sequence Files
                             Error

» Sequence quality Q is reported on a log scale
» Q10 is 1 error in 10
» Q20 is 1 error in 100
» Q30 is 1 error in 1000
» Q40 is 1 error in 10000
» Q50 is 1 error in 100000
        Capillary sequencing
» Individual reactions -> 96 capillary array
» PCR errors
» Cloning bias
» 1000-base reads
» 1-2 hour run time
» Accurate, Q30
» Low cost if want 1 read
» Low throughput, expensive to sequence
whole genomes
Next Generation sequencing

       Is massively parallel
Not limited to few reactions per run
   Next-Generation Sequencing




1 feature         1 chip,thousands or
1 template        millions of features
                  Output Mb-Tb
            Library prep




• Library
• Library
• Illumina Library




  P5



                       R1       R2                    P7
  Flowcell annealing
                       Primer   Primer site
                       site                   Flowcell annealing
• Illumina Library




  P5                   i5                      i7



                            R1       R2                     P7
  Flowcell annealing
                            Primer   Primer site
                            site                    Flowcell annealing
   Library Prep Approaches

1. Classical adapter ligation method

2. Transposon mediated

3. Inclusion of adapter sequences during
   PCR
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




     5’                              T                      A                   3’
     3’                              A                      T                   5’

                                         Make clusters and sequence
Nextera
Amplicon sequencing
454
                   454

» Started NGS (2005)
» First massively parallel sequencer
» Bought by Roche in 2007. Now
  discontinued
» Based on pyrosequencing of bead-
  bound DNA in microwells
» Fore-runner of Ion Torrent and
  Genapsys
         454/Roche Summary

» .7 Gb / run
» 700 base reads
» <24 hour run time
» $7,000 / Gb



Roche discontinued in 2016 – Too expensive
                  Pyrosequencing




» The incorporation of new bases releases inorganic pyrophosphate

 » A chemical cascade converts luciferin to oxy-luciferin + light
            Depositing DNA Beads into the PicoTiter™Plate

                                   Load Enzyme Beads

Load beads into
PicoTiter™Plate




                                   Centrifugation




                  44 μm
454 Technology - Sequencing Instrument
454 Data Example
             454/Roche Summary
» Long read lengths – good for amplicons and de-novo
sequencing
» High error rate near homopolymers
» Single end only
» .7 Gb / run
» 700-1000 base reads
» <24 hour run time
» $7,000 / Gb



Roche discontinued in 2016 – Too expensive
    Other Flow technologies

» Ion Torrent. As 454 but detects the H+
  released as a base is incorporated.



» Genapsys. As 454 but detects increase in
  impedence as a base is incorporated.
     Ion Torrent’s PGM




Capital cost $50,000
                  Ion Torrent
» Similar to 454 but detects H+ released as a base is
  added

» Prone to errors near homopolymers

» Not good for whole genome sequencing but useful
  for targeted sequencing as run times are short

» Used in a lot of clinical settings for disease panel
  sequencing
Ion Torrent’s Technology
                   DNA
                polymerase
                nucleotides
                                                well
                                            ion-sensing layer
                                            electronics layer

   DNA(n)+ nucl. = DNA(n+1) + PPi -> PPi + H+

      Flow through A then T then ... like 454
Ion Torrent Chip Drawing
             Ion Torrent
» Library prep like original 454
» Amplification on beads by emPCR
» CMOS chip detection
» Cyclic addition sequencing - pH changes
» Not single-molecule
 Ion AmpliSeq On-Demand Panels | Now 5,000 Pre-Designed, Pre-Tested Genes Available

                         Expanded Gene Content Across Disease Research Areas
                  2500

                  2000
     # of Genes




                  1500

                  1000

                   500

                     0




                         Average of 1154 genes per major UMLS disease research area category
                                        For Research Use Only. Not for use in diagnostic procedures.




42
 Ion GeneStudio S5 Series | Flexible Portfolio Configurable to Your Needs




              Ion GeneStudio™ S5                                                     Ion GeneStudio™ S5 Plus              Ion GeneStudio™ S5 Prime

                                                                                                       New                       New




                             Fast.                                                                Flexible.                    Powerful
                                                                                                                                  .
                                                                                                                                            New




      Ion 510™                                  Ion 520™                                 Ion 530™ Chip         Ion 540™ Chip            Ion 550™ Chip
         Chip                                      Chip                                  15–20 M reads         60–80 M reads           100–130 M reads
     2–3 M reads                               3–6 M reads                                Up to 600 bp          Up to 200 bp             Up to 200 bp
     Up to 400 bp                              Up to 600 bp
     For Research Use Only. Not for use in diagnostic procedures. * Throughputs based on 200bp sequencing




43
 Output and Turn-Around Time to Meet Your Lab’s Peak Volume Needs




                                                                Ion GeneStudio™ S5       Ion GeneStudio™ S5 Plus   Ion GeneStudio™ S5 Prime




                  Speed*                                                      19 hrs              10 hrs                    6.5 hrs


        Output (max/day):                                                   15 Gb/80 M        30 Gb/160 M                50 Gb/260 M


         Chips (max/day):                                                    1 x 540        2 x 540 or 1 x 550             2 x 550

 * Based off 540 chip – sequencing (2.5 hours) and analysis (varies) time



     For Research Use Only. Not for use in diagnostic procedures.




44
     $299k
     12-15M reads




45
46
Sequencing by Synthesis

with florescence detection
Illumina
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
iSeq100, HiSeq4000, Xten, NovaSeq
Since 2016 Illumina flowcells have been patterned
with clusters formed in a defined array of wells
ExAmp
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
   each end. And you can also perform sequencing
 reactions that read the sequence of the index in the
        introduced adapter. So how is this done
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
MiSeq i100
           Illumina

» Cheap $2-$300/Gb
» Highly accurate data mostly Q30
» Massively parallel. Millions/billions of
  reads
» Short read
The ownership of this material belongs to MGI，and without the permission of the owner, it shall not be directly release
or disclosed.


MGI All Rights Reserved Dissemination，distribution and copying is prohibited without authorization.
MGI sequencing chemistry
DNA nanoballs and cool MPS
DNBseq-T1+




12Tb in 22 hours
Approx $2/Gb
Upto PE300
              New
           Sequencers
                                           Illumina
                                           Chemistry X

Onso



                 Ultima UG100




       Element

                                      Singular
                                      S4


                                MGI
                              Comparison Table
                 Illumina        Illumina         Ultima UG100    Element Aviti       Singular G4       PacBio SBB
                 Novaseq         Nextseq

Instrument       $1.25M          $335k            $1.5M           $289k ($249K)       $350k             $99K

$/Gb             3 (10B), 2      20 (9 in 2024)   1               2-5                 8-10              4-12
                 (25B)

Accuracy         QQQ             QQQ              QQQ             QQQQ                QQQ               QQQQQ

Max read         2x150 (SP)      2x300            300 SE          2x300               2x150             200SE
length

Run Time for     24 hrs          48 hrs           18 hrs          48 hrs              19 hrs            48hrs
2x150 or 1x300

Flowcells        2               2                2               2                   4                 2

Yield/run        6000Gb,         30-360Gb         >4000Gb         480Gb               360Gb             150Gb
                 16000Gb

Other            Infinity long   Infinity long                    Non patterned,                        Non patterned
                 reads           reads                            loop long reads

Use case                                          Cheap           -high plex levels   Flexibility via   High accuracy
                                                  sequence for    –low                independent       applications,
                                                  big data        complexity          flowcells         high plex
                                                  applications,   -long reads                           potential
Element AVITI™
● ~$335K. $249K each if you order 3

● $2-$5/Gb. $1680 for 200-300Gb

● 2 flowcells. 2 x 150. 90% >Q40

● 2 x 300 available

● Sequencing by binding on RCA amplified template

● Loop synthetic long read

● Low duplicates

● No index hopping allowing for combinatorial indexing

● Better results with low complexity sequencing

● Can have long inserts >2kb




Images provided by Element Biosciences
Element Kits
 Avidity base chemistry (ABC)




Content and Images provided by Element Biosciences
AVITI System Architecture Enables
Maximum Run Flexibility
   Dual Independent Flow Cells       Individually Addressible Lanes




    Perform two parallel runs with   Sequence separate libraries or
      different run parameters         pools on a single flow cell
                  Cloudbreak Freestyle




Content and Images provided by Element Biosciences
Achieving Q50 with UltraQ




Content and Images provided by Element Biosciences
                Trinity: On Flow cell
                hybrid capture




Content and Images provided by Element Biosciences
Expert Mode HD: 20-70% more data
for FREE with higher polony density




Content and Images provided by Element Biosciences
Singular Genomics


●$10-$15/Gb
●2 x 150 in 19 hours
●4 x 4 lane flowcells. Each flowcell can be run and loaded
  independently.
●Uses similar SBS and clustering to Illumina
●No index hopping. No issue with low complexity
2




    Ultima
   Ultima
• $100 genome. $1/Gb
• SE 300 in ~14hr
• Flow based.
• Some indel errors around homopolymers
• 89% Q30
• Flow based sequencing on a 10” spinning disc
                                     Revolutionary new sequencing hardware

                            Camera




        Reagent dispenser

                                                    Spinning wafer on instrument
                                                                                   •   Low cost (standard substrate)

Wafer
                                                                                   •   ~10B reads per wafer (x2)


                                                                                   •   Fast and efficient reagent delivery


                                                                                   •   “Air gap” minimized contamination


                                                                                   •   Rotational optical scanning




                                                                                                                             Proprietary and Confidential
                                  A novel spin on sequencing chemistry
                                                 mnSBS

  Flow Chemistry                           Terminated chemistry   Mostly natural sequencing by synthesis

                      Diffusion




                                                                                                            Labeled




                                                                                                                 Unlabeled




Natural nucleotides                      Reversible terminator     Fluorescently labeled                      Mostly natural




                                                                   Long read length
                                                                   Fast cycle time
                                                                   Accurate
                                                                   Scalable
                                                                   Low cost
Transient detection                      End point detection

Static sensor                            Scanning




                                                                                                           Proprietary and Confidential
     Mostly natural chemistry combines advantages of
           flow chemistry with optical scanning
                                                      Median signals vs. homopolymer




                                                                          homopolymer level




• Majority nucleotides unlabeled to avoid quenching   • Endpoint detection significantly improves accuracy
• Minimal scarring supports longer reads              • Maintain signal linearity to at least homopolymer length 12
• Faster runs via 2min wash->image->cleave cycle      • Machine learning accounts for sequence context
         Mostly natural chemistry combines advantages of
               flow chemistry with optical scanning
                                                        Median signals vs. homopolymer




                                                                                     homopolymer level



•   Majority nucleotides unlabeled to avoid quenching   •   Endpoint detection significantly improves accuracy
•   Minimal scarring supports longer reads              •   Maintain signal linearity to at least homopolymer length 12
•   Faster runs via 2min wash->image->cleave cycle      •   Machine learning accounts for sequence context




                                                                                                                          Proprietary and Confidential
          Mostly natural chemistry combines advantages of
                flow chemistry with optical scanning
                                                        Median signals vs. homopolymer




                                                                                     homopolymer level



•   Majority nucleotides unlabeled to avoid quenching   •   Endpoint detection significantly improves accuracy
•   Minimal scarring supports longer reads              •   Maintain signal linearity to at least homopolymer length 12
•   Faster runs via 2min wash->image->cleave cycle      •   Machine learning accounts for sequence context




                                                                                                                          Proprietary and Confidential
         Mostly natural chemistry combines advantages of
               flow chemistry with optical scanning
                                                        Median signals vs. homopolymer




                                                                              homopolymer level




•   Majority nucleotides unlabeled to avoid quenching   •   Endpoint detection significantly improves accuracy
•   Minimal scarring supports longer reads              •   Maintain signal linearity to at least homopolymer length 12
•   Faster runs via 2min wash->image->cleave cycle      •   Machine learning accounts for sequence context


                                                                                                                          Proprietary and Confidential
PPM seq – 1 in a million VAF
        accuracy
PPM seq- library prep
     Roche SBX

- Nanopore sequencer enabled
 by acqusition of Genia and Stratos

- Launch 2026
- 500Mb/sec
- 15B reads in 4 hours
- 7B in 1 hour – fast mode
- Q39 for duplex libraries (200-
  300bp)
- Q23 for simplex (200-1500bp)

- Instrument $400-$600k?

- Consumable pricing = competitive

- Read the paper
DOI: 10.1101/2025.02.19.639056
Libraries are converted to expandomers
  Bases copied as XNTPs (50x bigger)
        Long Read Sequencers



               Oxford Nanopore flongle        Oxford Nanopore minION         Oxford Nanopore gridION




PacBio Revio



                    Oxford Nanopore P2 Solo
                                                       Oxford Nanopore P48
               Why Long Read

» Potential for higher diagnostic rate

» More complete coverage of genome

» Better assembly

» Haplotype linkage

» Simultaneous modified base detection
Long Read Platform Comparison
         Pacific Biosciences




Onso                     Revio
» Short Read sequencer   » Long Read sequencer
         PacBio Long Read

» Long Read Platforms
  RS>RSII>Sequel>SequelII>Revio

» SMRT. Single Molecule Real Time

» 3rd generation?
  Pacific Biosciences
Sequel II/IIe (2018-2022)
         » 8 million ZMWs/SMRT
         » $495K/$525 instrument
                                                                                                                Learn more:




» Revio system
Throughput



            480 Gb                                                  24 hour
            HiFi yield per run with SPRQ                            Sequencing time




            1,300 30x genomes / year
            2600 per year ta 20x




                                                                                      List price, USD
                                                                                                        $995/genome at 30x*
   * $995 for sequencing reagents for one Revio SMRT Cell, which has an
                                                                                      $599,000
                                                                                                        <$500 at 20x
   expected yield of 90 Gb, equivalent to a 30× human genome. Expected
   pricing subject to change, your local sales representative can provide
   detailed pricing in your currency.
                                                                                                                              117
Nov’ 24 Low Throughput Benchtop
                        Pac Bio Technology




       Individual ZMW                Laser light illuminates the ZMW




ZMW with DNA polymerase               ZMW with polymerase + nucs.
         PacBio Template Preparation




1   Anneal primer

2   Bind polymerase

3   Sequence
PacBio Sequencing
PacBio Sequencing


     » Some bases added very
       quickly and missed
     » Some wrong bases flirt with
       active site and go away
     » SMRT cell has millions of
       ZMWs (8M Sequel, 25M
       Revio)
Revio Polymerase Read Lengths
Accuracy
 Long read can access 193 medically
relevant genes that short read cannot
Epigenetics
Base Modifications
                          DETECTION OF DNA BASE MODIFICATIONS USING KINETICS

            Example: N6-methyladenine




•   SMRT Sequencing uses kinetic information from each nucleotide addition to call bases
•   This same information can be used to distinguish modified and native bases by comparing results of SMRT Sequencing to an in silico
    kinetic reference for incorporation dynamics without modifications.




                                                                                           Flusberg et al. (2010) Nature Methods 7: 461-465
Revio variant calling and                                          Accuracy, F1%

methylation performance        100
                                            99.95     99.95            99.41     99.44
                                                                                                  95.19     95.59

                                 80



                                 60



                                 40



                                 20
  +5mC




                                   0
                                                SNVs                       Indels                       SVs

                                                       Sequel IIe system            Revio system


             PEG3
                            HG002 at maternally imprinted PEG3 locus
                            Data for internal beta testing https://downloads.pacbcloud.com/public/revio/2022Q4/HG002-
                            rep3/analysis/HG002.m84005_220827_014912_s1.GRCh38.bam
                            Variant calling measured against Genome in a Bottle benchmarks, HG002                       131
MAS-Seq: high-throughput, full-length single-cell sequencing




                           Full-length, 10x
                          single-cell cDNA




                                                  MAS-Seq for 10x Single Cell 3’ kit
                                                          (102-659-600)

                                                      • 16x concatenation
                             A                                                                             Q
                                              B                 C        N                O            P
                                       B’              C’           D’           O’               P’




                                        A         B         C       D        N        O       P        Q




 https://www.biorxiv.org/content/10.1101/2021.10.01.462818v1
                                     Cell atlas, single-cell sequencing



                                                                                                            3
                                                        scRNA-Seq




                            scIso-Seq


      of human multi-exon                                                                                                          of brain expressed
                                                                          isoforms per gene
95%   genes have more                                      >7             on average2                                    2,900     genes are heritable
      than one isoform1                                                                                                            at isoform level4




      1https://www.sciencedirect.com/science/article/pii/S2001037020305341;
      2https://www.biorxiv.org/content/10.1101/2022.06.08.495354v1.full; 3https://www.pnas.org/doi/full/10.1073/pnas.2114326118;
      4https://www.medrxiv.org/content/10.1101/2022.10.18.22281204v1
Comparison of PacBio with other
         approaches
      Pacific BioSciences
   Sequel/Revio Applications
» Long read applications
» De Novo sequencing
» Full length cDNA sequenicng
» Haplotyping
» Variant calling with access to repetitive regions


» DNA modification studies
            Pacific Biosciences

» Single polymerase mol. in a 20nm hole
» Watch incorporation in real time
» ~2 bases per second
» Yield 120Gb
» ~$5-10/Gb
» HiFi reads 15-20kb
PacBio Onso
●   Released 2023
●   Most accurate short read
●   90%> Q40, Q50 possible
●   $99K current offer price
●   $4-12/Gb
●   100Gb/run
●   1x200 or 2 x 150 in 48hr
●   Sequencing by binding
●   Accuracy to 0.001% VAF
    without UMIs
Sequencing by Binding
SNV and Indel accuracy are better than any other
platform
SBB demonstrates >4×                                 100%
                                                                                 1.4x
                                                                               sensitivity
improvement in sequencing                            90%

efficiency                                           80%

                                                     70%

                                                     60%




                                       Sensitivity
                                                     50%

                                                     40%
       6,000× non-UMI SBB sequencing
       exceeds >24,000× SBS UMI                      30%
       sequencing at 0.05% and 0.1%                                                                             SBB 6,000×
                                                     20%                                                        SBS 24,000×

                                                     10%

                                                      0%
                                                                   0             0.05              0.1            0.25              0.5

                                                                              Variant allele %

                                                       Data based on internal testing. >4× improvement in sequencing efficiency relative to SBS
                                                                                                                                                  140
Nanopore Sequencing
           Oxford nanopore

» Sequences single molecules of DNA as travel
  through pore

» Can also identify modified bases and
  sequence RNA directly

» Reads typically 5-50kb but some much longer
  (4Mb record)
ONT Simplex (1D) Library prep
             Flow cell design          Nanopore




» Application-Specific Integrated
  Circuits (ASICs), MinION ASIC
  contains 512 channels
                                             Synthetic
                                             membrane


» Each channel is surrounded
 by 4 pores & records only 1
                                           ASIC
 at a time

» 512 pores max recorded at the time
Oxford Nanopore Technologies




      Imagine 5-base words = 1024 current levels
             ONT: The squiggles




     A G G T G C A T T G C T T G A G T T C T T T C A G T T A C T




Slide courtesy of David Buck. WTCGH
Assuming 5mer current signals




    From Szalay & Golovchenko, Nat. Biotech., 2015.
ONT basecalling with machine learning
R10. A dual head nanopore to help resolve
             homopolymers


 CsgF




CsgG




        From Van der Verren et al., Nature Biotech 2020
 ONT Sequencing
performance graphs
ONT accuracy
ONT accuracy
ONT accuracy
Direct sequencing of modifications
          minION
$1999. Yields upto 48Gb ~$5/Gb.
          512pores.
Connected minION
Mk Ic
        Mk Id based on ipad
        pro
GridION. For service sector




$67000
Flongle flow cell adapter
    $90 for 2-3Gb
                 PromethION
            24 or 48 flowcells with 12000 pores




~$7-16/Gb
       PromethION P2 Solo




~$7-16/Gb
    ONT unique applications

» Ultra-long reads (>100kb reads possible)
» “Run until” done. W.I.M.P
» Selective reads
» Mobile sequencing
» Direct RNA sequencing
» Direct methylation detection over wide range
of DNA and RNA modifications
         So. Which to choose?

» Budget
» Technical fit
» Applications
» Throughput
» Peers
» Space
Any Questions ?

   mq1@sanger.ac.uk
