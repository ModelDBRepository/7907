# September 24th, 2015

dendritica-1.0, dendritica-1.1 and the documentation are now available directly from ModelDB. Please note that these are the original versions from 2001, which will not run without modifications on current versions of NEURON. However, the source code may be useful as a collection of algorithms for the analysis of structure-function relations in neurons.

Arnd Roth arnd.roth at ucl.ac.uk

# May 17th, 2002

Installation note:
Michael Hines had found that dendritica worked at least in its interactive mode with a unix (and linux) version (5.2) of Neuron by

1) installing iv as described at the neuron installation page
2) after unpacking the nrn source code change the line
```c
#if !defined(WORDS_BIGENDIAN)
```
to
```c
#if defined(WORDS_BIGENDIAN)
```
in `./nrn-5.2/src/ivoc/ivocvect.cpp`
3) finish the installation of neuron as usual.

Also note that dendritica "2. Getting Started" instructions in "2.1 A sample session" has the following changes for Neuron 5.2. After `nrnivmodl` is run in
`./dendritica-1.0/batch_back/back/mod/kvz_naz`

the folder (e.g. sparc/ or i686/ i.e. named after your machine) created by nrnivmodl, with all its contents and subdirectories, should be moved up to the back/ directory. Then to start Neuron and dendritica cd to the back/ directory and type
```bash
nrngui gui.hoc
```
(a minus sign on the end of the command is not needed).

---

# Dendritica

## Software tools for studying dendritic signalling

This page provides links to *Dendritica,* a package of software tools for studying propagation of action potentials in dendrites, to be used in conjunction with the simulator [NEURON](http://www.neuron.yale.edu/). The programs are based on those used for the simulations described in the following paper:

[Vetter, P., Roth, A. & Häusser, M.](http://jn.physiology.org/cgi/content/abstract/85/2/926) (2001). Action potential propagation in dendrites depends on dendritic morphology. *Journal of Neurophysiology,* 85: 926-937.

*Dendritica* is available as a complete package which will enable you to interactively reproduce the simulations in the paper. The programs have been written for the Linux or Unix environments, and require [NEURON 4.1.1](http://www.neuron.yale.edu/ftp/neuron/versions/). You will need approximately 100 MB of disk space for the entire installation. Note that to run all the programs successfully, you may also need to make several minor modifications to the NEURON source code (see documentation above).

---

2025-05-27 – Standardized to Markdown.