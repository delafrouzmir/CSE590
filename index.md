# CSE590 First Assignment

## Wolfram Mathematica

[Wolfram Mathematica](https://www.wolfram.com/mathematica/), or [Mathematica](https://www.wolfram.com/mathematica/) is a mathematical computation program used in many scientific, engineering, mathematical, and computing fields. It was created by Stephen Wolfram and is developed by [Wolfram Research](http://www.wolfram.com/company/) of Champaign, Illinois. The [Wolfram Language](https://www.wolfram.com/language/) is the programming language used in Mathematica.
Mathematica covers more than 5000 functions covering all mathematical functions as well as computing areas such as neural network, machine learning, visualization, data science, etc. It uses powerful and fast algorithms and hardware as well as parallel programming to achieve higher precision and more speed.

## Platforms
Mathematica can be used on any platform. With [Wolfram Cloud app](https://itunes.apple.com/us/app/wolfram-cloud/id978701305) anyone can use Mathematica with just a browser. It can be installed on Desktop as well as mobile apps. [WolframAlpha](https://www.wolframalpha.com/) which works on Mathematica technology is also an interface available for anyone with access to an internet browser. There are also widgets for it available on android and iOS phones.

## Parallelism
Mathematica uses parallelism both in its own implementations of functions and providing an environment for user-level parallel programming.

### Parallelism and Multi-threading
Mathematica version 5.2 (2005) added automatic multi-threading when computations are performed on multi-core computers. This release included CPU specific optimized libraries.
Mathematica started using supercomputer-style cluster computing support from [Pooch](http://daugerresearch.com/pooch/whatis.shtml) created by [Dauger Research](http://daugerresearch.com/index.shtml) in 2006. The Supercomputing Engine for Mathematica (SEM, a.k.a. the PoochMPI Toolkit) enables Wolfram Research's Mathematica to be combined with supercomputer-compatible Pooch clustering technology.  Following Message-Passing Interface (MPI), the Supercomputing Engine creates a standard way for every Mathematica kernel in the cluster to communicate with each other directly, rather than a master-slave model. After locating, launching, and coordinating Mathematica kernels on a cluster, the Supercomputing Engine creates and supports an "all-to-all" communication topology.

### User-level Parallel Programming
[GridMathematica](https://www.wolfram.com/gridmathematica/) was introduced in 2002 to allow user level parallel programming on heterogeneous clusters and multiprocessor systems. Until 2010 parallel computing technology was included in all Mathematica licenses including support for grid technology such as Windows HPC Server 2008, Microsoft Compute Cluster Server, Sun Grid, [CUDA](https://en.wikipedia.org/wiki/CUDA) and [OpenCL](https://en.wikipedia.org/wiki/OpenCL) GPU hardware. In version 8 generating C code was added.

## Performance
Since Mathematica uses parallelism in a variety of algorithms and applications, we cannot tell for sure what is the ratio of sustained to peak performance. I also could not find the specifications of algorithms, but the technologies used are described above.

### Resources
- [https://www.wolfram.com/mathematica/](https://www.wolfram.com/mathematica/)
- [https://itunes.apple.com/us/app/wolfram-cloud/id978701305](https://itunes.apple.com/us/app/wolfram-cloud/id978701305)
- [http://daugerresearch.com/pr/poochmpimath.shtml](http://daugerresearch.com/pr/poochmpimath.shtml)
- [http://daugerresearch.com/pooch/mathematica.shtml](http://daugerresearch.com/pooch/mathematica.shtml)
- [http://daugerresearch.com/index.shtml](http://daugerresearch.com/index.shtml)
- [https://en.wikipedia.org/wiki/Wolfram_Mathematica](https://en.wikipedia.org/wiki/Wolfram_Mathematica)
- [http://blog.wolframalpha.com/2010/12/06/mathematica-becomes-a-wolframalpha-interface/](http://blog.wolframalpha.com/2010/12/06/mathematica-becomes-a-wolframalpha-interface/)
- [https://www.wolfram.com/gridmathematica/](https://www.wolfram.com/gridmathematica/)
