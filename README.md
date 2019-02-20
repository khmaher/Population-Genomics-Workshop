### Katy Maher, Victor Soria-Carrasco, Toni Gossmann, Henry Barton


## Connecting to Iceberg from Windows

You can connect to Iceberg through your [web browser](https://myapps.shef.ac.uk/sgd/index.jsp?langSelected=en&SGD_Token=Epc6zWBl1mzYDM~hmN3q51gRAYIEkWvf) by entering your username and password.

Once you have logged in you should be on a head node. You must log in to a worker node by typing:

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

source .bash_profile
```

Note: **The repository is only accessible from the working nodes**, so you won’t have access
to any program from the head nodes.



If the repository is set up correctly, you should see the following message every time you log in a working node:

```markdown
Your account is set up to use the Genomics Software Repository
    More info: http://soria-carrasco.staff.shef.ac.uk/softrepo
```







You can use the [editor on GitHub](https://github.com/khmaher/Population-Genomics-Workshop/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/khmaher/Population-Genomics-Workshop/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
