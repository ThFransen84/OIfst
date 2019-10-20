Old Irish Morphological Finite-State Transducer (FST), mainly for verbs.
====

The code has been implemented by using the finite-state compiler foma, developed by Mans Hulden. For download instructions and documentation see https://fomafst.github.io/.

The development of an Old Irish fst was part of my Ph.D. thesis, see http://www.tara.tcd.ie/handle/2262/89498, Chapter 4. 

The code consists of lexicon files (.lexc), rules (.rule), scripts (.script), stems (.txt), and binary files (.fst), put in their respective directories. The directory structure should be maintained if making changes to files. Running the file 'shell_script' in the main folder handles file location to create binary .fst files. The binary files are included in the directory 'fst' and are ready to use (e.g. 'load oiv.fst' in foma); creating the FSTs by running the script is only necessary when making changes to e.g. stem lists.
