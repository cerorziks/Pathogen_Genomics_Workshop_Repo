       NGS Library
       Construction

         Michael Quail
        mq1@sanger.ac.uk
WTAC
              Talk Outline


» What is a NGS sequencing library?
» How are they made? Options and considerations.
» Problems
Sequencers
1   tcctggcatc agttactgtg ttgactcact cagtgttggg atcactcact ttccccctac
61 aggactcaga tctgggaggc aattaccttc ggagaaaaac gaataggaaa aactgaagtg
121 ttactttttt taaagctgct gaagtttgtt ggtttctcat tgtttttaag cctactggag
181 caataaagtt tgaagaactt ttaccaggtt ttttttatcg ctgccttgat atacactttt
241 caaaatgctt tggtgggaag aagtagagga ctgttatgaa agagaagatg ttcaaaagaa
301 aacattcaca aaatgggtaa atgcacaatt ttctaagttt gggaagcagc atattgagaa
361 cctcttcagt gacctacagg atgggaggcg cctcctagac ctcctcgaag gcctgacagg
421 gcaaaaactg ccaaaagaaa aaggatccac aagagttcat gccctgaaca atgtcaacaa
481 ggcactgcgg gttttgcaga acaataatgt tgatttagtg aatattggaa gtactgacat
541 cgtagatgga aatcataaac tgactcttgg tttgatttgg aatataatcc tccactggca
Sequencing workflow


Library
 Library   Sequencing    Analysis
 Prep       Sequencing    Analysis
  Prep
Library
 Library   Sequencing    Analysis
 Prep       Sequencing    Analysis
  Prep
Library
 Library   Sequencing    Analysis
 Prep       Sequencing    Analysis
  Prep
Library
 Library   Sequencing    Analysis
 Prep       Sequencing    Analysis
  Prep
» Original DNA




• Library
• Library
• Illumina Library




  P5                   SP 1



                                     SP2                   P7
  Flowcell annealing   Primer site
                                     Primer site   Flowcell annealing
      Illumina Library Insert sizes
          Exome, targeted, RNAseq, ChiP, ATAC
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

    Reads need to be just long to span common repeat elements eg AluI
    with unique sequence on either side so can map
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
 add adapter sequences to 5’ end of primers
Illumina Library Prep
How do you go about making a
good library?
QC
          Input DNA for NGS

• Properly quantified. Flourimetric methods preferred

• DNA from appropriate source

• DNA >40kb required for long read applications
      Pure DNA 260:280 close to 1.8
      Nanodrop reading should be approx. 2x qubit

• RNA RIN>8
Initial Characterisation/QC

• Spectrophotometry (inc nanodrop)
Initial Characterisation/QC

• Spectrophotometry (inc nanodrop)
 Initial Characterisation/QC
• Gel     M       M




• Qubit
Advanced Analytical
Fragment Analyzer
Advanced Analytical Femto Pulse
Agilent Tapestation
 Agilent Tapestation for sequencing
             library QC
Offer range of kits for different input and size ranges
                    Generic library prep workflow 2006

DNA

Shear
   cleanup
End-repair
   cleanup
A-Tail
   cleanup
Ligate to adapter
    cleanup
Size select

PCR
    cleanup
Quantitate + Characterise
Streamlining generic library prep workflows

DNA                          DNA

Shear                        Shear
   cleanup                      cleanup
End-repair                   End-repair and A-tail
   cleanup
A-Tail                       Ligate to adapter
   cleanup                       cleanup
Ligate to adapter            Size select
    cleanup
Size select                  PCR
                                 cleanup
PCR                          Quantitate + Characterise
    cleanup
Quantitate + Characterise
Shearing
DNA Shearing by Acoustics


  AFA tube
                         Focused acoustics




                                             Reproducible
       Programmable shearing
Shearing

                           Other options

     • Matrical sonicman (96 well sonication)
       www.matrical.com
     • Bioruptor www.diagenode.com              physical
     • Episonic. www.epigentek.com
     • Nebulisation (single sample)
     • Fragmentase (NEB)
     • Nextera (Epicentre)
                                                enzymatic
Shearing

                           Other options

     • Matrical sonicman (96 well sonication)
       www.matrical.com
     • Bioruptor www.diagenode.com              physical
     • Episonic. www.epigentek.com
     • Nebulisation (single sample)
     • Fragmentase (NEB)
     • Nextera (Epicentre)
                                                enzymatic
Shearing Problems

 - Enzymatic shearing can result in variation in fragment size
 between samples
    -Can be dependent on amount, GC content or presence of contaminants
 - Sonication based methods can generate heat leading to AT
   dropout
 - Fragments smaller than the read length can give rise to low ratio
   of mapped reads.
 - Smaller fragments cluster more efficiently so if multiplexing
   libraries they should be sheared to similar fragment size ranges
   else some will be represented more than others in final sequence
   output.
After shearing

    3’           3’

    5’           5’



    3’           3’

    5’           5’
End-Repair

p
            3’

            5’
        p
    Tailing

p
              A 3’

A                 5’
              p
     Ligation of Illumina Adapters

               p
                       A 3’

               A           5’
                       p
5’                              p    3’
           T

                                T
3’         p                         5’
     After Ligation


5’                    3’
     T          A

     A           T
3’                    5’



                 5’
                       T


                 3’        p
             SPRI: Ampure
    »    http://www.beckmangenomics.com/products.html


DNA

Shear

End-repair

A-Tail

Ligate to adapter

PCR
                            »   Advantages:
Quantitate + Characterise       Easy to automate, some size selection properties

                            »   Disadvantages:
                                A bit fiddly to do manually
          Amplification
     5’                              3’
          T                A

          A                T
     3’         4 - 10 cycles, PCR   5’

5’
5’   5’    T                A         3’   3’
3’         A                T              5’



5’         T                A              3’
3’   3’    A                T         5’   5’
                                           5’
Multiplexing
Multiplexing
      Tag sequences
      Tag 1    CGTGAT
      Tag 2    ACATCG
      Tag 3    GCCTAA
      Tag 4    TGGTCA
      Tag 5    CACTGT
      Tag 6    ATTGGC
      Tag 7    GATCTG
      Tag 8    TCAAGT
      Tag 9    CTGATC
      Tag 10   AAGCTA
      Tag 11   GTAGCC
      Tag 12   TACAAG
                                    Multiplexing on Illumina




@IL22_1561:1:1:1771:914
TTTTTTCAATACAATTTCATCTCTAATTTCAATTCAGCCTAA
+
>>>>7>>>>>>>>>>>>>>>>>>>:>5>>>96>+>>7;>>>>
@IL22_1561:1:1:1222:1105
ATGATATCATCTACACGGTTTAAAAATTCTGGACGGCTGATC
+
>>;>>>>>>>;>>>>>55>>>>>>>>>>>>+2>>8>>>>>57
@IL22_1561:1:1:1438:709
                                              TAG      Strain
ACACCGATGACAATAATTGTTCCAATATCTGTAACAAAGCTA
                                              CGTGAT   HGSA942
+
                                              ACATCG   3HK
<<<<<2<<2<<<<<<<<<)'<<<<<<<<<<+<;;7<)<<2<<
                                              GCCTAA   CHI59
@IL22_1561:1:1:1671:1462
                                              TGGTCA   CHI61
TGCAAGAACATTAGACAACGTATCTTCAATCGTTTATACAAG
                                              CACTGT   BK2491
+
                                              ATTGGC   TUR9
>>7>:>:>>7>>7/:>>>7/.7>>>>>57>>0>>>>>>7>>>
                                              GATCTG   HU25
@IL22_1561:1:1:1168:891
                                              TCAAGT   HU109
AATGGAAATCAAACTATAACTTCAACACTAAATGAGAAGCTA
                                              CTGATC   HSJ216
+
                                              AAGCTA   FFP103
>>>:7>>>>>>>>>>>>>>>>>>>>>>>>>>>>0>>>>>>>>
                                              GTAGCC   ICP5062
@IL22_1561:1:1:1097:1281
                                              TACAAG   GRE4
TAAAAGTATAACTTTCCATCACCAAAGTCAGAATTTACATCG
+
>>>>>>>>>>>>>>>>>>>>>>>>8>8>>>>>>>>>>>>>>>
Multiplexing Options



                       Truseq stubby Adapters


                       Stubby Adapters available from IDT
Full length Adapters
                       Indexing primers from:
Available from:        Illumina
                       IDT
Illumina               NEB
IDT                    Roche
NEB                    Quantabio
Roche                  Tecan
Quantabio              Perkin Elmer
Tecan                  Eurofins
Perkin Elmer           etc
etc
NGS Library Prep Kits
     -Enzymatic or physical shearing options
     -With or without adapters/primers
     -PCR or PCRfree
  NGS library kit manufacturers

» NEB                » Agilent
» Illumina           » Tecan
» IDT                » Thermo
» Twist bioscience   » Takara
» Roche/Kapa         » Watchmaker
» Qiagen             » Meridian
» Agilent            » Quantabio
» Tecan              » Thermo
NEB UltraExpress FS DNA
   library kit E3340L
Size Selection
           Size Selection

» Gel
» Pippin Prep
» Ampure
             SPRI: Ampure
    »    http://www.beckmangenomics.com/products.html


DNA

Shear

End-repair

A-Tail

Ligate to adapter

PCR
                            »   Advantages:
Quantitate + Characterise       Easy to automate, some size selection properties

                            »   Disadvantages:
                                A bit fiddly to do manually
SPRI purification
    Working with SPRI Beads

»   SPRI (Solid Phase Reversible Immobilization) Beads
»   Paramagnetic beads made of polystyrene surrounded by a layer of
    magnetite, which is coated with carboxyl molecules
»   Reversibly bind DNA in the presence of the “crowding agent” polyethylene
    glycol (PEG) and salt (20% PEG, 2.5M NaCl is the magic mix).
»   PEG causes the negatively-charged DNA to bind with the carboxyl groups on
    the bead surface.
»   DNA fragment size affects the total charge per molecule with larger DNAs
    having larger charges; this promotes their electrostatic interaction with the
    beads and displaces smaller DNA fragments.
»   The size of fragments eluted from the beads is determined by the
    concentration of PEG, which is determined by the mix of SPRI:DNA at a
    given ratio.
»   The lower the ratio of SPRI:DNA the higher the molecular weight
    of the fragments bound to the beads.
Double sided SPRI



• By implementing a combination of good shearing with SPRI and “reverse” SPRI, one can select a size range:




Source: Enseqlopedia from Broad Institute and Illumina
Phased Cleanup: removal of adaptors


                                                                      Discard                        Add Bead
      Add beads                                                                        Add
                                                                        SN                         Reconstitution
        (0.7X)                                                                       0.1X TE
                                                                     (adaptors)                     Buffer (0.8X)




    DNA sample          Library binding   Separate beads              Keep Library          Elute DNA            Rebind DNA
        after           to SPRI beads        from SN                 on SPRI beads         from beads           to SPRI beads
   PCR enrichment            5 min             5 min                                                                5 min



          Remove       2x Wash                                                                    Transfer SN
                                                             Add                                  to new tube
            SN           with                              0.1X TE                                  (Library)
         (adaptors)   80% EtOH




Separate beads              Wash DNA         Air dry             Elute DNA            Separate beads            Cleaned up
   from SN                  2x 30 sec      bead pellet           In 0.1X TE              from SN                  Library
     5 min                                   5 min                  2 min                  5 min
Phased Bead Cleanup for UltraExpress RNA workflow

        Add 70 µl (0.7X)                                                     Remove tubes from magnet
     resuspended beads to
    the 100 µl PCR reaction




•   Pipet mix or quick                              Without disturbing the
                              Incubate on magnet
    vortex/centrifuge                              beads carefully remove
                                 for 5 minutes
•   Room Temp 5 minutes                            and discard supernatant
                                                                                 Add 100 µl of 0.1X
                                                                                 TE and pipet to mix
 Phased Bead Cleanup for UltraExpress RNA workflow




Add 80 µl (0.8X) NEBNext Bead Reconstitution Buffer to the 100 µl resuspended beads




    Pipet mix and            Incubate on magnet         Discard                       200 µl (80% ETOH)
incubate at RT 5 min                5 min             supernatant                       wash 2X for 30
                                                                                           seconds
  Phased Bead Cleanup for UltraExpress RNA workflow


  Be sure to remove all                  Note: Do not allow beads to over dry or crack
residual 80% ETOH and
  incubate up to 5 min




When beads are ready
elute with 0.1X TE and
    incubate at RT



                              Separate                        Transfer eluate
                             on magnet                         to a new tube
NEB phased cleanup from
NEBNext UltraExpress™ FS DNA Library
Prep Kit
                     Add 0.8x
 0.7x                NEB bead
            100ul    suspension
            0.1xTE   buffer
Ampure Size Selection
Analysis / Library QC
Final Analysis
Problems
What can possibly go wrong!!
Adapter Dimer
Small Insert Contamination
Small Insert Contamination
Larger fragments??




                 17/9/12
      When primers deplete
P5 and P7 can anneal but internal
 fragments don’t match up so are
        single stranded
        P5                                                              P7




Problem: DNA binding dyes used in quantitation eg Qubit and in tapestation/bioanalyzer
bind ds DNA so don’t properly quantify
Need to qPCR to properly quantify
Bias
           P. falciparum with original Illumina sample prep




GC content

coverage
Required Sequence Coverage
   Required Sequence Coverage




30x sequencing depth required for efficient calling of heterozygous variants
Aim for 95% > 15x so you have sufficient coverage over most
positions to call variants
   Required Sequence Coverage




                    15x


If we get bias the amount of regions with low coverage will increase and we
wont be able to call variants so we then have a choice of whether to fail
those samples or sequence again
         Contributors to bias

» Heat

» Shearing method

» PCR

» Target enrichment
         Contributors to bias

» Heat
  » Heat steps >65C can irreversibly denature AT rich regions

» Shearing method

» PCR

» Target enrichment
         Contributors to bias

» Heat
  » Heat steps >65C can irreversibly denature AT rich regions

» Shearing method

» PCR

» Target enrichment
         Contributors to bias

» Heat
  » Heat steps >65C can irreversibly denature AT rich regions

» Shearing method

» PCR
  » Need right Enzyme and conditions

» Target enrichment
    Coverage across a section of B. pertussis genome



        %GC




Coverage depth




                                          Kapa HiFi
                                          Phusion
                                          noPCR

                 See https://www.nature.com/articles/nmeth.1814
                 and https://doi.org/10.1099/mgen.0.001228
Recommended PCR enzymes
    for NGS library prep
» Quantabio repliQa
» Watchmaker Equinox
» Takara Premier plus

For Long Read
» Quantabio repliQa
» Merck KOD Extreme
         Contributors to bias

» Heat
  » Heat steps >65C can irreversibly denature AT rich regions

» Shearing method

» PCR
  » Need right Enzyme and conditions

» Target enrichment
  » 100x coverage required for hybrid capture target enrichment
  » 1000x coverage required for PCR based targeted sequencing
Sample Representation Bias
Sample representation




          8.7%CV
Sample representation




          8.7%CV
Sample representation




          13%CV
Measuring Sequencer Size Bias Using REcount: A Novel
            Method for Highly Accurate
     Illumina Sequencing-Based Quantification




                                          MiSeq
                                          NextSeq
                                          Novaseq
                                          iSeq
   The secret to a low sample
      representation CV
» Standardise as much as possible

  » Automation
  » Reliable quantification step
  » Standardise DNA input amounts
  » Accurate pipetting
  » Control fragment sizes
Efficiency
Library Prep Efficiency
Illumina library efficiency
Illumina library efficiency
Library quantification prior to
         sequencing
Library quantification prior to
         sequencing
  Options:
  qPCR
  Agilent bioanalyser, Caliper
  Labchip GX
  Qubit
qPCR quantification



                                                     Libraries of
     200pM                                           unknown
             20pM

                          0.2pM
                                                     concentration
                    2pM
                                  0.02pM
                                           0.002pM
         Introduction to the Library Prep Workflow
                                    NEBNext UltraExpress® DNA




Max Fritsch | Field Application Scientist
Streamlining the library prep workflow




                                   ONE        ONE
DNA Fragmentation                [adaptor]   cycle #

                    End Repair   Adaptor      PCR
                                                        Clean-
                    dA-Tailing   Ligation     Amplify
                                                        up
    Enrichment,
RNA Fragmentation
    & cDNA
    generation
       NEBNext UltraExpress® DNA Library Prep
                     Workflow



5′                                     3′
3′                                     5′   Fragmentation
                                            •   Random fragmentation overhangs can be 1-4 bases on the 5’ end, blunt ends or 3’
                                                overhangs
                                            •   Incubation time determines fragment size
5′                3′   5′              3′
3′                5′   3′              5′
                                            End repair
         5′                     3′          •   Enzymatic activity that fills in 5’ overhangs and chews back 3’ overhangs to create
         3′                     5′
                                                blunt ends

                                            dA-Tailing
                                            •   Enzymatic activity to ‘A’-tail the blunt-ended DNA fragments to prepare them for
                                                adaptor ligation
5′              A 3′   5′            A 3′
3′ A              5′   3′ A            5′

         5′                   A 3′
         3′ A                   5′
       NEBNext UltraExpress® DNA Library Prep
                     Workflow




                                                      Adaptor Ligation
5′
3′ A
                    A 3′
                      5′
                           5′
                           3′ A
                                               A 3′
                                                 5′
                                                      •   Ligation of the T overhang of the hairpin adaptor to the A overhang of the fragmented
           5′                     A 3′
                                                          DNA
           3′ A                       5′




                                                      Hairpin Adaptor
                                                      •   Higher conversion rates
                                                      •   Greater complexity
                                                                                                                   3′

           5′                         3′
                                                      •   Minimizes adaptor dimer formation                        5′ T
                                                                                                                                     U

                T                 A
       U                                   U
                A                 T
           3′                         5′
NEBNext UltraExpress® DNA Library Prep
              Workflow




           5′           3′
                T   A
       U                     U
                A   T
           3′           5′


                                             ‘U’ excision
                                             •   USER enzyme removes in a series of enzymatic reactions the uracil base to
                                                 open the NEBNext hairpin adaptor in preparation for PCR


                                      USER



  5′                             3′
                T   A
                A   T
  3′                             5′
                                       U
      NEBNext UltraExpress® DNA Library Prep
                    Workflow




                                                                        5′
                5′                                      3′
                          T               A                        P7
                                                              BC
                                                   3′
                     3′
           BC
                          A
                                                                             PCR enrichment
      P7                                  T


 5′
                3′                                      5′                   •   Amplifies adaptor ligated DNA
                                                                             •   Adds sample specific Barcode/Index
                                  st
                              1        PCR Cycle



                                                                             Cycle 1: the barcoded P7 PCR primer anneals, but there is still sequence
                                                                             missing on both strands
                5′                                           3′
                3′                                                      5′



5′                                                      3′
           3′                                           5′
      NEBNext UltraExpress® DNA Library Prep
                    Workflow




      P5   BC
 5′              3′
            3′                                        5′



5′                                         3′              PCR enrichment
                                3′
                                            BC   P5
                                                      5′
                                                           •   Amplifies adaptor ligated DNA
                                                           •   Adds sample specific Barcode/Index
                          nd
                      2        PCR Cycle



                                                           Cycle 2: Barcoded P5 primer anneals; the result is one full length strand

 5′                                                   3′
            3′                                        5′



5′                                         3′
3′                                                    5′
     NEBNext UltraExpress® DNA Library Prep
                   Workflow



5′                                   3′
       3′                            5′



5′                              3′
3′                                   5′

                                          PCR enrichment
                   rd
                  3 PCR Cycle
                                          •   Amplifies adaptor ligated DNA
                                          •   Adds sample specific Barcode/Index
5′                                   3′
3′                                   5′


5′                                   3′
                                          Cycle 3+: Both strands are full length; DNA is amplified by PCR
3′                                   5′


5′                                   3′
3′                                   5′


5′                                   3′
3′                                   5′
      NEBNext UltraExpress® DNA Library Prep
                    Workflow




                         T
                     U
      P5   BC                               5′
 5′             3′                                    Library cleanup
                                       P7

                             3′
                                  BC                  •   Removes enzymes and buffer from the PCR
                                                      •   Removes any leftover adaptor dimer
5′                                               3′
3′                                               5′   •   Removes PCR primers
5′                                               3′   •   Phased Clea-up: double clean-up
3′                                               5′


5′                                               3′
3′                                               5′


5′                                               3′
3′                                               5′
           Quick Reminder: Best
            Practices in the Lab
1. Thaw the buffers on top of the ice or in your hand and vortex to mix.

2. DO NOT vortex enzymes!

3. Mix enzymes by flicking the tube gently and inverting the tube.

4. Quick spin down the tubes containing the enzymes and buffers.

5. Keep enzymes and thawed buffers on ice.

6. Keep reactions on ice unless it is specified to stay at room temp (RT)

7. Mix reactions thoroughly by pipetting up and down as indicated in
  protocol.
Part Two
           Talk Outline


» Libraries for other sequencing
  platforms.
» Types of NGS sequencing library?
» Automation of library prep
Sequencers
Sequencers
PacBio Library Prep
                                                      Library
                                                      Preps


                  Fragment DNA




                  Repair Ends




A-Tailing




Ligate Adapters                     Ligate Adapters


                                                       T        A

                                                       A            T
                      Exonuclease
                   digestion of linear
                          DNA




                        2 x SPRI




                  Quantify and QC
ONT 1D Library prep
Sequencers
Alternative standard library
       prep methods
 Next generation
enzymatic shearing
      Ultra II NEB FS DNA:
      stem


             Kit: Enzymatic fragmentation, combined with Ultra II DNA Library Prep reagents


                         Fragmentation/                         Clean up/
                         End Repair/             Adaptor        Size                                       Clean up
                         dA-Tailing              Ligation       Selection         Amplification



                                          Hands-on: 8-14 min.    Ultra II DNA FS input amounts:
                                          Total: 1.5-3 hrs       100 pg – 0.5 µg, with a single protocol


        Robust, easy to use and compatible with input DNA in water and standard DNA buffers (TE, Tris-HCl).

        Capable of generating a wide range of insert sizes, by varying incubation time.

        Uses the same fragmentation protocol, for all input amounts and GC contents.

        Produces high yields of high quality libraries.



UltraII FS. Shearing relatively unaffected by contaminants, GC
content and input amount. Controllable fragment sizes. Can use
for low input.
Nextera
               Nextera XT

» It works but
  » Can be expensive
  » Size of fragments sensitive to DNA amount,
    GC content and contaminants
     » Small inserts. Adapter. Lower mappability
     » DNA not in correct size range
     » More variable insert sizes
     » More variable coverage when multiplexing
            Illumina NextFlex
          Okay but insert sizes 300bp




Nextera Flex. Much much better than old Nextera and XT. Shearing
relatively unaffected by contaminants, GC content and input amount.
Expensive and not too easy to tune fragment sizes.
Other library types
              What is Targeted
               Sequencing??
“Targeted resequencing is a variation of re-sequencing where only a
  small subset of the genome is sequenced, such as the exome, a
   particular chromosome, a set of genes or a region of interest”
NoPCR (PCRfree)
                                       Amplification bias
                                                      B.pertussis

Theoretical P.falciparum       No-PCR P.falciparum
                                                                    Sequence data from both
                                                                    raw and mapped no-PCR
                                                                    datasets represent much
                       standard P.falciparum
                                                                    closer the base
                                                                    composition of the
                                                                    P.falciparum 3D7 genome
                                                                    than the standard datasets.




                      theoretical GC content

                      raw
                                  no-PCR libr GC content
                      mapped



                      raw
                                  standard libr GC content
                      mapped
No-PCR library preparation :
                   FP1 and FP2’:part of the adapter sequence

       +


                   Enrichment for fully ligated templates during the
                   cluster generation stage
                   Non-ligated templates cannot attach to the flowcell
                   Semi-ligated templates cannot form a bridge and thus
                   clusters




                  More crucial than for the standard library
                  preparation are:
                  Sample DNA quality and quantity
                  Quantification of libraries with lower concentration
RNA seq
             RNA seq Approaches


» 3’ gene expression via oligo dT priming
» Full length cDNA
» Single cell 3’, 5’ or probe based

» Enrichment and rRNA depletion
  » Typically oligodT
  » Probe based for globin, RNA or other
    depletion
                                  RNA seq
               Illumina cDNA protocol
                                            RNA
                                            mRNA
                                            Fragment - metal ions
needs good quality DNA free RNA             cDNA synthesis
Ideally RIN > 8                             cDNA
                                            End-repair

                                            A-Tail
                                            Ligate to adapter

                                            Size select/Gel purify

                                            PCR

                                            Quantitate + Characterise
                      Directional RNA seq
                  dUTP/USER protocol



Parkhomchuk et al.,
NAR. 2009, 37 (18)
                      small RNA

                              RNA
                              miRNA
                              Ligate 3’ adapter
                              Ligate 5’ adapter
                              RT
                              PCR
                              Size select/Gel purify
                              Quantitate + Characterise


» Notes
-need 2ug total RNA
           ChIP
Chromatin Immunoprecipitation
HiC
ATAC and DNAse Seq
Methyl Seq
NEB EM-Seq
How Many Libraries?
      Sequence yield


                       9000Gb

               500Gb


       100Gb



1Gb
              Yellow Answers
                To make all these LIBRARIES is



             lot of work
Samples from different sources
Different levels of complexity
Large sample sets
Headache!!
Automation
Approaches to Automation
High throughput manual
Low throughput automation
Agilent Magnis – 8 sample automation
  Low throughput automation



                Apollo 324
http://www.wafergen.com/products/apollo-324

                                                        Tecan MagicPrep NGS
                                                    http://www.tecan.com/magic




                Agilent Magnis
           http://www.agilent.com             PE BioCule
High throughput automation


  Hamilton Star
                               Tecan fluent




                                              Agilent Bravo
                  Revvity Sciclone NGS
 Beckman i7
      Introductory systems?




Opentrons flex        SPT Firefly
Any Questions ?

   mq1@sanger.ac.uk
