Test post
---------

`testpost.md`—- put this in the `posts` directory. 

It cites works that are only available in the three bibliographies listed below. 

To test the `exclusive_bibliography`, change the `bibliography` key in the metadata block in test.md to `exclusive_bibliography`. This will load the corresponding bibliography and prevent the others from being loaded. This might seem like an odd thing to do, but because of the way citation keys are usually generated (author + name + disambiguator), clashes could easily arise between a default bibliography used on most of the site and one that's needed for the odd page here and there. 

If you delete the `csl`field in the metadata block, the csl specified in the pelicanconf file will be loaded instead. 


Bibliographies
--------------

# Pelican-Pandoc-Samples

place the following files in `content/assets/`:

- metadata.bib : this will be referenced from the metadata block
- defaultfrompelicanconf.bib : this will be referenced from the pelican conf file

place this in `posts/`:

- testpost.bib

Add to pelicanconf.py
---------------------

csl files can be downloaded or referenced from here: https://www.zotero.org/styles

```python

# list of paths to default bibliographies
DEFAULT_BIBLIOGRAPHIES = ['content/assets/bib/defaultfrompelicanconf.bib']

# path to default csl
DEFAULT_CSL = 'https://www.zotero.org/styles/chicago-author-date'

```


