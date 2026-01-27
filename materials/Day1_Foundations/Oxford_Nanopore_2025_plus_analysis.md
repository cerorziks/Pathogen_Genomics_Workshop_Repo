Oxford Nanopore sequencing
Oxford Nanopore sequencing

Objective:
• To gain a greater depth of understanding of the principles of working
  with Long Reads and ONT sequencing

• To understand the ONT offering with regards to making an informed
  choice for your project
Oxford Nanopore sequencing




       Image c/o Oxford Nanopore, https://www.youtube.com/watch?v=3UHw22hBpAk
Q20+

 • Combination of latest Nanopore(R10.4.1) and Library Construction kit (“Kit 14”) will give
   single strand accuracy of “99.3%” and duplex (where both strands of DNA are

 • basecalled) of “~99.9%” Duplex = methylation information & high quality basecalls from

      single strand –no need for consensus (which can obscure rare variants)
 • This is currently in early access testing and not fully commercially available Some
 • applications, e.g. Direct RNA sequencing, may not be available as quickly as others



 N.B. Illumina NovaSeqstats suggest >75% reads at Q30 at 2x250 or >90% reads at Q30 at 2x50bp
 https://emea.illumina.com/systems/sequencing-platforms/novaseq/specifications.html
                                                                                                Q10 = 90% Q20 = 99% Q30 = 99.9%
DNA Extraction Methods
                                         Magnetic
                                          beads?
     Kit?                    Nucleus
                            isolation?
                                                     Bead
                Phenol
              Chloroform?                           beating?


You cannot get long reads from short fragments!
DNA extraction methods

The four S’s!

Safety                       What is the best
                             method for your
Species                       application?
 Suitable (cost,equipment)
Scale up (or size)
Assessing your DNA fragments

Purity                   Nanodrop

Length                   Tapestation or FemtoPULSE
                         or gel

Amount
                         Qubit
Library construction
                                                       L iga tio n Suited to maximising
                            Rapid
                                                                   data yield
          Suited to fieldwork or ultralongsequencing
Image c/o Oxford Nanopore
Optional Fragmentation

Not recommended for some applications, e.g. short
fragments, PCR products

Can be useful when some very long fragments are present
but high throughput is priority

Options include G-TUBE (historically recommended by ONT),
needle shearing, Megaruptor
Ligation vs Rapid

                    Ligation   Rapid
     Yield Time
     Cost Data
     quality
     Robustness
Multiplexing

 Make best use of a flow cell capacity by   Component      Sequence
                                            NB01   AAGAAAGTTGTCGGTGTCTTTGTG
 combining >1 sample together Each          NB02   TCGATTCCGTTTGTAGTCGTCTGT
                                            NB03   GAGTCTTGTGTCCCAGTTACCAGG
 sample is “labelled” with a known          NB04   TTCGGATTCTATCGTGTTTCCCTA
 DNA sequence                               NB05   CTTGTCCAGGGTTTGTGTAACCTT
                                            NB06   TTCTCGCAAAGGCAGAAAGTAGTC
 Oxford Nanopore barcodes are longer        NB07   GTGTTACCGTGGGAATGAATCCTT
                                            NB08   TTCAGGGAACAAACCAAGTTACGT
 than Illumina, at 24 bases
                                            NB09   AACTAGGCACAGCGAGTCTTGGTT
                                            NB10   AAGCGTTGAAACCTTTGTCCTCTC
 This allows confidence despite the
                                            NB11   GTTTCATCTATCGGAGGGAATGGA
 higher per-base error rate, and makes      NB12   CAGGTAGAAAGAAGCAGAATCGGA


 use of Oxford Nanopore’slong reads
Basecalling

Current or recently announced basecallers now allow:

   •Real time methylation information
   •Demultiplexing of samples


   •Accurate sequencing of short fragments (>20bp)
Oxford Nanopore Platforms and Products
Oxford Nanopore sequencing




       MinI ON Up               GridI O N Up    Pro methI O N Up to

         to 50Gb                 to 250Gb       220Gb per flow cell
                                               10.5Tb per instrument




    Image c/o Oxford Nanopore
Images center and right c/o Oxford Nanopore
Why is it so small?

   Other machines need to have cameras and lasers to take pictures of the
   DNA

   They need to have moving parts to add chemicals to synthesise the
   DNA

   The MinIONmeasures electrical signals from DNA that is already
   present
MinION

Don't forget cost
of computer!




   Prices c/o Oxford Nanoporestore, taken 27/03/2025
GridION




  Image c/o Oxford Nanopore
GridION




  Image c/o Oxford Nanopore
PromethION
                              48 flow cells

                              Each flowcell
                              originally “50Gb”
                              now maximum is
                              290Gb

                              Up to 14Tb of
                              sequence

                              Rapidly evolving

  Image c/o Oxford Nanopore
PromethION




  Image c/o Oxford Nanopore
P2

A “mini”
PromethION


Also as “solo” model –
plugs into GridIONor
computer




     Image c/o Oxford Nanopore
Flongle
                             48 Flongle Flow cells



                                        Adapts MinION to take
                                        cheap, low throughput flow
                                        cells

                                        Closed store BUT still
                                        available




 Image c/o Oxford Nanopore
Q Line

SO 9001:2015 certified manufacturing process

12 months guaranteed supported software & consumables
Clearly mapped out upgrades


Same price as standard devices & consumables

Allows in house validation of assays for long term use
Where has Oxford Nanopore been used?
http://www.nature.com/news/pint-sized-dna-sequencer-impresses-first-users-1.17483
Image c/o NASA, USA
                                                                                                      Image from The Guardian Online
https ://www. the g ua rdi a n. c om/s c i e nc e /2016/ f e b/03/f rom- e b ol a - to- zi ka - ti ny- m obi l e - l a b- g i ve s - re a l - ti
me - dna - da ta - on- outbre a ks
SARS-CoV-2
Concluding thoughts
Oxford Nanopore sequencing

Advantages              Disadvantages
Portable                Can require highly pure DNA
Rapid                   Can require large amountsof input DNA
Low start up costs      Less supported analysis
Native DNA sequencing
Long read
Multiplexing options
Fleet of sequencers
Floatation

Oxford Nanopore Technologies floated on the
London Stock Exchange in 2021

Currently valued at ~£979 million ($1.26 billion –for comparison Illumina
~$12.96 billion) down from about £2.2 billion (Illumina down from $31
billion)

What does this mean for your science?
-perhaps greater visibility of how the company is performing
-otherwise, not much
Additional technologies




                          press.office@sanger.ac.uk
•All scripts/software = open source

•Slides & links available on your course webpage

•Questions?

   kj6@sanger.ac.uk

   @kim_judge_
Analysis session
Objective

 Check our data
 Assemble bacterial data generated using the latest Oxford Nanopore
 Chemistry (as used this morning)
 Check completeness of assembly
 Investigate assembling other samples
 Each genome can have many assemblies!
Why?
                  head
                  tail
Let’s find out    ls –l

reads and check   assembly-stats


them out
Depth of Coverage
and
Theoretical Depth of Coverage
1. Install minimap2 and miniasm
  Search for the website

  https://github.com/lh3/miniasm


  Copy the commands into your terminal



  git clone https://github.com/lh3/minimap2 && (cd minimap2 && make)

  git clone https://github.com/lh3/miniasm && (cd miniasm && make)
2. Run the overlap


minimap2/minimap2 -x ava-ont </path/to/sample1.fastq> </path/to/sample1.fastq> > <sample1.paf>
3. Run the assembly


 miniasm/miniasm -f </path/to/sample1.fastq> <sample1.paf> > <sample1.gfa>


 Minimap2 & miniasm will work with compressed (zipped) data files, so you can try running:


 minimap2/minimap2 -x ava-ont </path/to/reads.fq> </path/to/reads.fq> | gzip -1 >
 <reads.paf.gz>

 miniasm/miniasm -f <reads.fq> <reads.paf.gz> > <reads.gfa>
4. Assess the assembly
    Process the assembly to get fasta format
    awk '$1=="S" {print ">"$2"\n"$3}' sample1.gfa > sample1.fa
    Then Try:
    head
    wc-l
    tail
    ls -l
    assembly-stats
Overview
 minimap2/minimap2 -x ava-ont </path/to/sample1.fastq> </path/to/sample1.fastq> > <sample1.paf>

 miniasm/miniasm-f </path/to/sample1.fastq> <sample1.paf> > <sample1.gfa>

 awk '$1=="S" {print ">"$2"\n"$3}’ <sample1.gfa> > <sample1.fa>

 assembly-stats <sample1.fa>
5. Try on other samples
You could consider submitting part of your finished assembly to BLAST

Google NCBI BLAST

Click Nucleotide BLAST

Paste in the box
Round up and final questions
