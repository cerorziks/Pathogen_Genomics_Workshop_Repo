Bioinformatics
Essentials


Dr. Jacqui Keane
    @drjkeane
drjkeane@gmail.com
Overview
▸ Bioinformatics Software   ▸ Bioinformatics Pipelines
Learning Outcomes
▸ You can expect to be able to:
    ○ Describe what a software package manager is and why are useful
    ○ Install a software package manager (conda/mamba)
    ○ Install bioinformatics software with the conda package manager
    ○ Describe what a workflow manager is and why useful
    ○ Install Nextflow and run a Nextflow pipeline
Overview
▸ Bioinformatics Software
Bioinformatics Software

▸ Many bioinformatics software

▸ Complex to install and manage
   −   - e.g. conflicting dependencies


▸ Use software package manager
Conda
▸ Automates the process of installing software and their
  dependencies

▸ Software applications available via channels

▸ A channel online locations of where packages are stored
e.g. conda-forge, r, bioconda
Bioconda channel
Conda environments
▸ A separate space (box) where you install specific versions of
  software/set of softwares

▸ Prevent conflicts between different softwares by allowing you
  to manage dependencies separately

▸   Create, activate, and switch between environments easily
Mamba
▸ A software package manager similar to Conda

▸ Faster and uses less memory, good for installing software
  faster and using less computer resources

▸ Fully compatible with conda
    Demo
    ▸ Bioinformatics Software
         ▸   Install conda from:
             https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html
         ▸   Install mamba from:
             https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html
         ▸   Use conda to install samtools
$ conda info --envs
$ conda list
$ samtools
$ conda create -n samtools-1.21 samtools=1.21.0
$ conda info –envs
$ conda activate samtools-1.21
$ conda list
$ samtools
$ conda deactivate
Overview
           ▸ Bioinformatics Pipelines
Bioinformatics Pipelines

▸ Automate analysis using
  a pipeline
   - e.g. bash script


▸ Re-write the pipeline for
  different platforms

▸ Use workflow/pipeline
  management system
Nextflow
▸ Use it to write and run data-intensive workflows/pipelines

▸ Nextflow consists of a
    −   language to write pipelines
    −   engine to run pipelines

▸ Write a pipeline once and run everywhere!
nf-core
▸ Community effort to collect a set of best practice analysis
  pipelines built using Nextflow
Sequera Platform (Nextflow Tower)
▸ Manages and tracks the executions of Nextflow pipelines
Sequera Platform (Nextflow Tower)
     Demo
     ▸ Bioinformatics Pipelines                         $ conda create -n nf-pipelines
                                                        $ conda activate nf-pipelines
           ▸    Install Nextflow and nf-core            $ conda install nextflow nf-core
                                                        $ nf-core pipelines list
           ▸    Install nf-core pipeline                $ nf-core pipelines list | grep -i
                - fetchngs                              rna

           ▸    Run the fetchngs pipeline




$ wget
https://github.com/sylabs/singularity/releases/download/v4.2.2/singularity-ce_4.2.2-noble_amd64.deb
$ sudo dpkg -i singularity-ce_4.2.2-noble_amd64.deb
$ nextflow run nf-core/fetchngs -profile singularity –input ids.csv –outdir .
Questions?
