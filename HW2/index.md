# CSE590 Second Assignment

## Parallel Programming Model in OpenSHMEM


## 	Suggested Multi-threading Models for OpenSHMEM
### Communication Context
Communication contexts define the set of rules and the way of communication between different PEs, or Remote Memory Access routines, Atomic Memory Operations, and memory ordering routines. Using communication contexts will allow the user to:
- manage the overlap of computations with communications in single-threaded PEs, for example pipelining computations and communications.
- manage the ordering and completion of communications in multi-threaded PEs independently from the PEs, for example the isolation of threads from the multi-threaded PE which has created them in order to reduce the overheads of communication between PEs.

### Types of communication contexts
- SHMEM_CTX_DEFAULT: by default, the communication contexts are sharable between the threads of a multi-threaded PE. This means the context can be used concurrently by the threads of a PE.
- SHMEM_CTX_SERIALIZED: available in the multi-threaded model, in this mode the context is not used concurrently by all the threads of a PE. It is up to the user to make sure that operations involved with this mode are serialized.
-	SHMEM_CTX_PRIVATE: available in the multi-threaded and serialized mode, in this mode the context is only usable by the thread that created it. 


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
