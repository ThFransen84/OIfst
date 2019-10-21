Old Irish Morphological Finite-State Transducer (FST), mainly for verbs
====

The FST has been implemented in foma, a finite-state compiler and C library developed by Mans Hulden. For download instructions and documentation see https://fomafst.github.io/.

The code consists of lexicon files (.lexc), rules (.rule), scripts (.script), stems (.txt), and binary files (.fst), put in their respective directories. The directory structure should be maintained if making changes to files and running the file 'shell_script', which:
1. contains unix commands to handle the insertion of stem lists into se_empty.lexc (to create se.lexc), and 
2. invokes foma script files (which in turn contain rules) to create binary .fst files. 

The directory 'fst' contains saved binary files; running 'shell_script' is only necessary after (typically) updating the stem lists to update the fst files, of which there are two:
1. oiv.fst: Old Irish verbs
2. oiAll.fst: additional frequent words.

The development of an Old Irish FST was part of my Ph.D. thesis, for which see http://www.tara.tcd.ie/handle/2262/89498. Chapter 4 (pp. 55–104) describes the implementation in great detail. A list of errata for the entire thesis can be found under projects, at https://github.com/ThFransen84/OIfst/projects/1.
