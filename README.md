Old Irish Morphological Finite-State Transducer (FST), mainly for verbs
====

<img src="https://raw.githubusercontent.com/ThFransen84/OIfst/master/logo.png" alt="FST logo" width="200" height="100">

The development of an Old Irish FST was part of my Ph.D. thesis, which is available [here](http://www.tara.tcd.ie/handle/2262/89498). The abstract (with proper text encoding), as well as a list of *errata*, can be found under [*Projects*](https://github.com/ThFransen84/OIfst/projects) relative to this repository. Chapter 4 (pp. 55–104) in the thesis describes the implementation in great detail.

The FST has been implemented in *foma*, a finite-state compiler and C library developed by Mans Hulden. For download instructions and documentation see https://fomafst.github.io/.

The code in this repository consists of lexicon files (`.lexc`), rules (`.rule`), scripts (`.script`), stems (`.txt`), and binary files (`.fst`), put in their respective directories. The directory structure should be maintained if making changes to files and running the file `shell_script`, which
1. contains unix commands to handle the insertion of stem lists into `se_empty.lexc` (to create `se.lexc`), and 
2. invokes *foma* script files (which in turn contain rules) to create binary `.fst` files. 

The directory *fst* already contains the latest saved binary files; running `shell_script` is therefore only necessary after updating files (typically the stem lists), to create new `.fst` files, of which there are two:
1. `oiv.fst`: Old Irish verbs
2. `oiAll.fst`: additional frequent words found in an Early Irish narrative text (see Chapter 5 of my Ph.D. thesis).
