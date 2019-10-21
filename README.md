Old Irish Morphological Finite-State Transducer (FST), mainly for verbs
====

The code has been implemented by using the finite-state compiler foma, developed by Mans Hulden. For download instructions and documentation see https://fomafst.github.io/.

The development of an Old Irish FST was part of my Ph.D. thesis, see http://www.tara.tcd.ie/handle/2262/89498, Chapter 4. 

The code consists of lexicon files (.lexc), rules (.rule), scripts (.script), stems (.txt), and binary files (.fst), put in their respective directories. The directory structure should be maintained if making changes to files and running the file 'shell_script' in the main folder. The latter consists of unix commands to handle the insertion of stem lists in se_empty.lexc and invokes foma script files to create binary .fst files.  The binary files are included in the directory 'fst' and are ready to use (e.g. 'load oiv.fst' in foma); in other words, running 'shell_script' is only necessary when making changes to e.g. stem lists to update the binary fst files.
