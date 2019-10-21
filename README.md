Old Irish Morphological Finite-State Transducer (FST), mainly for verbs
====

The FST has been implemented in foma, a finite-state compiler and C library developed by Mans Hulden. For download instructions and documentation see https://fomafst.github.io/.

The code consists of lexicon files (.lexc), rules (.rule), scripts (.script), stems (.txt), and binary files (.fst), put in their respective directories. The directory structure should be maintained if making changes to files and running the file 'shell_script' in the main folder. The latter consists of unix commands to handle the insertion of stem lists in se_empty.lexc and invokes foma script files to create binary .fst files.  The binary files are included in the directory 'fst' and are ready to use (e.g. 'load oiv.fst' in foma); in other words, running 'shell_script' is only necessary when making changes to e.g. stem lists to update the binary fst files.

The development of an Old Irish FST was part of my Ph.D. thesis, for which see http://www.tara.tcd.ie/handle/2262/89498. Chapter 4 (pp. 55–104) describes the implementation. A list of errata for the thesis can be found under projects, at https://github.com/ThFransen84/OIfst/projects/1.
