# CSE590 Second Assignment

## Parallel Programming Model in OpenSHMEM
OpenSHMEM provides parallelism by allowing multiple Processing Elements (PEs) to start in parallel and then communicate and synchronize the remotely accessible data objects across PEs. Each PE has remotely accessible, as well as private data objects. Figure 1 depicts the memory model in OpenSHMEM.
![Memory model in OpenSHMEM](HW2_Memory_Model.PNG)
As shown in the above picture, the remotely accessible data consists of:
- Global or static variables
- Data on the symmetric heap (data allocated by shmem_malloc in C and C++)
All other variables are private to the PE they are created in.
Communication and data sunchronization between PEs can be done through major memory routines such as:
1. Remote Memory Access (RMA) routines: enable a PE to _Put_ some local (private) or public (symmetric) data on a public data object of another PE, or to _Get_ some public data from another PE to copy into a local or public data object. Read more about RMA here: []()
2. Atomic Memory Operations (AMO): Read more about AMO here: []()
All data transfers in OpenSHMEM are one-sided, meaning that the PE starting a communication does not wait for the other PE to respond to complete the transfer. This allows the overlap of communication and computation since a PE does not wait for other PEs and can continue its work which reduces the runtime due to the reduction of data trasnfer latencies.


## 	Suggested Multi-threading Model for OpenSHMEM
### Communication Context
Communication contexts define the set of rules and the way of communication between different PEs, or Remote Memory Access routines, Atomic Memory Operations, and memory ordering routines. Using communication contexts will allow the user to:
- manage the overlap of computations with communications in single-threaded PEs, for example pipelining computations and communications.
- manage the ordering and completion of communications in multi-threaded PEs independently from the PEs, for example the isolation of threads from the multi-threaded PE which has created them in order to reduce the overheads of communication between PEs.

### Types of communication contexts
- SHMEM_CTX_DEFAULT: by default, the communication contexts are sharable between the threads of a multi-threaded PE. This means the context can be used concurrently by the threads of a PE.
- SHMEM_CTX_SERIALIZED: available in the multi-threaded model, in this mode the context is not used concurrently by all the threads of a PE. It is up to the user to make sure that operations involved with this mode are serialized.
-	SHMEM_CTX_PRIVATE: available in the multi-threaded and serialized mode, in this mode the context is only usable by the thread that created it. 


### Resources
- [https://www.wolfram.com/mathematica/](https://www.wolfram.com/mathematica/)
- [https://itunes.apple.com/us/app/wolfram-cloud/id978701305](https://itunes.apple.com/us/app/wolfram-cloud/id978701305)
- [http://daugerresearch.com/pr/poochmpimath.shtml](http://daugerresearch.com/pr/poochmpimath.shtml)
- [http://daugerresearch.com/pooch/mathematica.shtml](http://daugerresearch.com/pooch/mathematica.shtml)
- [http://daugerresearch.com/index.shtml](http://daugerresearch.com/index.shtml)
- [https://en.wikipedia.org/wiki/Wolfram_Mathematica](https://en.wikipedia.org/wiki/Wolfram_Mathematica)
- [http://blog.wolframalpha.com/2010/12/06/mathematica-becomes-a-wolframalpha-interface/](http://blog.wolframalpha.com/2010/12/06/mathematica-becomes-a-wolframalpha-interface/)
- [https://www.wolfram.com/gridmathematica/](https://www.wolfram.com/gridmathematica/)
