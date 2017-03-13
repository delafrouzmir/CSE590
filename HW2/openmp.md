Notes on interaction between OpenMP and OpenSHMEM:
1. Like MultiThreading-MPI works, OpenSHMEM functions can be also altered in order to incorporate idle threads in OpenMP to do useful jobs.
Like the endpoints idea in MPI, OpenSHMEM library can introduce endpoints in order to let every thread in the system act like a PE and cooperate in collective operations (like reductions).
Like MPI, different approaches can be studied regarding how to deal with multi-threading in OpenSHMEM: whether to use global locks in all methods, or use locks per objects, or use fine-grained locks in functions, or even lock-free based operations (Global, Brief Global, Per-object, and Lock-free methods).  At the hardware level, multi-channel NICs can be studied too.
Four levels of support are introduced in MPI: single, funneled, serialized, and multiple. Based on Cray’s proposal for OpenSHMEM, they believe funneled and serialized are deemed to be obsolete. 
Based on ideas in “Casper” (http://www.mcs.anl.gov/project/casper/), a group of cores is responsible for transferring data in a node for RMA operations. The same idea can be extended to OpenSHMEM and let a group of cores be responsible, but it needs underlying runtime to be aware of the idea. 
In environments that are oversubscribed by tasks, Casper might have advantages over allowing each task to communicate. A group of cores is in charge to do all the communications required by PEs. 
Investigating how manycore environments (specifically, Xeon Phi) impact the performance of OpenMP and OpenSHMEM in hybrid programs.
