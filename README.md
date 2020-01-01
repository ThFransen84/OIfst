Old Irish Morphological Finite-State Transducer (FST), mainly for verbs
====

<img src="https://raw.githubusercontent.com/ThFransen84/OIfst/master/logo.png" alt="FST logo" width="200" height="100">

The development of an Old Irish FST was part of my Ph.D. thesis, for which see this [Wiki](https://github.com/ThFransen84/OIfst/wiki/Ph.D.-thesis-(2019)).

The FST has been implemented in *foma*, a finite-state compiler and C library developed by Mans Hulden. For download instructions and documentation see https://fomafst.github.io/.

The code in this repository consists of lexicon files (`.lexc`), rules (`.rule`), scripts (`.script`), stems (`.txt`), and binary files (`.fst`), put in their respective directories. The directory structure should be maintained if making changes to files and running the file `shell_script`, which
1. contains unix commands to handle the insertion of stem lists into `se_empty.lexc` (to create `se.lexc`), and 
2. invokes *foma* script files* to create binary `.fst` files. 
* script files typically read in external lexicon and rule files, and (in this implementation) also employ variables previously defined in other script files and as such present in memory.

The directory *fst* already contains the latest saved binary files; running `shell_script` is therefore only necessary after updating files (typically the stem lists), to create new `.fst` files, of which there are two:
1. `oiv.fst`: Old Irish verbs
2. `oiAll.fst`: additional frequent words taken from the Early Irish narrative text *Táin Bó Fraích* (see Chapter 5 of my Ph.D. thesis).
