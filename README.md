### Katy Maher, Victor Soria-Carrasco, Toni Gossmann, Henry Barton

## Linux tutorials and cheat sheets
Before you start it is useful to get familiar with some basic linux commands.

Although we will provide the necessary commands for the practicals we will teach, they assume knowledge of the basics. Below are some useful links to go through before the start of the workshop or revisit as a reminder after. 

[Online command-line ‘bootcamp’](http://rik.smith-unna.com/command_line_bootcamp/?id=g4gaphxtmz4)

[Basic tutorial](http://openwetware.org/wiki/Butlin:Unix_for_Bioinformatics_-_basic_tutorial)

[Linux and Shell cheatsheet](http://rcg.group.shef.ac.uk/courses/linux/shell-cheatsheet.html)


## Connecting to Iceberg from Windows

You can connect to Iceberg through your [web browser](https://myapps.shef.ac.uk/sgd/index.jsp?langSelected=en&SGD_Token=Epc6zWBl1mzYDM~hmN3q51gRAYIEkWvf) by entering your username and password.

Once you have logged in you should be put onto the head node. You must log in to a worker node by typing:

```markdown
qsh
```

No work should ever be conducted on the head node. This is just a gateway to the worker nodes. 

If you are on the head node you should see something like this displayed in your comand line:

```markdown
[cs4ab35@iceberg-login3 ~]$
```

Once logged in to a worker node you should see something like this:

```markdown
[cs4ab35@node063 ~]$
```

You can exit your worker node by typing:

```markdown
exit
```

To log off the cluster after you have exited your worker node type:

```markdown
exit
```

## Accessing the software repository 

Before starting the practical sessions we need to access the [Genomics Software Repository.](http://soria-carrasco.staff.shef.ac.uk/softrepo/)

The Genomics Software Repository is basically a collection of software located in a shared folder on Iceberg, the High Performance Computing Cluster at the University of Sheffield. Although any Iceberg user can access and use it, it has been primarily established as a way to develop and support the analytical infrastructure of the Molecular Ecology Group at the Department of Animal and Plant Sciences. The repository comprises a collection of ready-to-use programs for NGS and population genetic/genomic analysis (e.g. BEAST, Colony, STACKS, GATK). Its main advantage is that it removes the necessity for the user to install commonly used programs in their home folder.

First we will add the path to the genomics software repository to your $PATH environmental variable. This will save us having to use the whole path each time we want to use some software:

```markdown
echo -e "if [[ -e '/usr/local/extras/Genomics' ]];\nthen\n\tsource /usr/local/extras/Genomics/.bashrc\nfi" >> $HOME/.bash_profile

```

If the repository is set up correctly, you should see the following message 
```markdown
Your account is set up to use the Genomics Software Repository
    More info: http://soria-carrasco.staff.shef.ac.uk/softrepo
```
after you type:

```markdown
source .bash_profile
```

You should also get this message every time you log onto a working node.

Note: **The repository is only accessible from the working nodes**, so you won’t have access
to any program from the head nodes.


## Schedule and links to exercises

|Session|Date and time|Teacher|
|---|---|---|
|OPTIONAL: Introduction to Linux|Tuesday 26th March 11-1pm||
|[SNP calling and filtering overview](https://henryjuho.github.io/uspopgen/)|Tuesday 26th March 4-5.30pm|Henry Barton|
|[Population genomic analyses using PopGenome](http://tonig-evo.github.io/workshop-popgenome/)|Wednesday 27th March 10.30-1pm|Toni Gossmann|
|[Genetic structure](https://khmaher.github.io/popgenomicsworkshop-structure)|Wednesday 27th March 2-3.30pm|Katy Maher|
|[Detecting selection](https://visoca.github.io/popgenomworkshop-hmm/)|Wednesday 27th March 4-5-30pm|Victor Soria-Carrasco|
|[Genome-wide association studies (GWAS)](https://visoca.github.io/popgenomworkshop-gwas_gemma)|Thursday 28th March 9-12.30pm|Victor Soria-Carrasco|
|[OPTIONAL EXTRA: GWAS using GenABEL](https://github.com/mestocks/gwas-workshop)|To be done in own time|Victor Soria-Carrasco|

NB we will not have time to go through the **GWAS using GenABEL** exercise during the workshop but it is included above as an extra worked example.


