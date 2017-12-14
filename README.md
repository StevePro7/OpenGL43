# OpenGL43
Examples for the OpenGL Red Book

Download
https://www.ics.uci.edu/~gopi/CS211B/opengl_programming_guide_8th_edition.pdf

Add ChapXX folder
Add ChapXX filter
Copy Main to ChapXX folder
Rename all Main* to whatever project is called e.g. 01-Triangles
Add Existing Project to Solution
Remove Main.cpp reference and re-add renamed cpp file e.g. 01-Triangles.cpp
Right click newly added project
Working Directory change default $(ProjectDir) to $(TargetDir)
Build + Run


DEBUG
01.
LINK : warning LNK4075: ignoring '/INCREMENTAL' due to '/LTCG' specification

Linker | General
Enable Incremental Linking
Yes (/INCREMENTAL)


Linker | Input
Ignore Specific Default Libraries
MSVCRT;%(IgnoreSpecificDefaultLibraries)

Reference:
https://stackoverflow.com/questions/3007312/resolving-lnk4098-defaultlib-msvcrt-conflicts-with


RELEASE
01.
All 3 functions were compiled because no usable IPDB/IOBJ from previous compilation was found.

Linker | General
Enable Incremental Linking
NO (/INCREMENTAL:NO)

Reference:
https://social.msdn.microsoft.com/Forums/sqlserver/en-US/b8f2dac5-0bdb-4cec-9c11-e7dfee760d4b/what-combination-of-vc-14-options-triggers-fast-link-time-code-generation?forum=vcgeneral


Linker | Optimization
References					Yes (/OPT:REF)
Enable COMDAT Folding		Yes (/OPT:ICF)
Link Time Code Generation	Use Link Time Code Generation (/LTCG)