For the latest stable version, please use the redesign-threading-model branch. We will update the master branch soon.

For the project description, please visit the wiki branch, and check out ProjectHome.md. There is also a tutorial, MaestroTutorial.md.

Maestro is an "operating system" for orchestrating network control applications. Maestro provides interfaces for implementing modular network control applications to access and modify state of the network, and coordinate their interactions. Maestro is a platform for achieving automatic and programmatic network control functions using these modularized applications. Although this project focuses on building an OpenFlow controller using Maestro, Maestro is not only limited to OpenFlow networks. The programming framework of Maestro provides interfaces for:

Introducing new customized control functions by adding modularized control components.
Maintaining network state on behalf of the control components.
Composing control components by specifying the execution sequencing and the shared network state of the components.
Moreover, Maestro tries to exploit parallelism within a single machine to improve the system's throughput performance. The fundamental feature of an OpenFlow network is that the controller is responsible for every flow's initial establishment by contacting related switches. Thus the performance of the controller could be the bottleneck. In designing Maestro we try to require as little effort from programmers as possible to manage the parallelization. Instead Maestro handles most of the tedious and complicated job of managing work load distribution and worker threads scheduling. By design Maestro is both portable and scalable:

Developed in Java (both the platform and the components) - Highly portable to various operating systems and architectures.
Multi-threaded - Takes full advantage of multi-core processors.
Maestro currently provides the control components for realizing either a learning switch network, or a routed network using OpenFlow switches. Some components such as the command line console, etc, are still not full-fledged. We plan to further enrich and enhance the functionality of Maestro in future releases. Notice that Maestro is licensed under the GNU Lesser General Public License version 2.1. Google-project's LGPL directs only to the version 3, so we make it explicit here that Maestro is licensed under LGPL v2.1.

As a starter, please check the Tutorial Wiki Page.

For more details about using and programming Maestro, please refer to:

Using and Programming Maestro.
For details about the multi-threading design and performance evaluation of Maestro, please refer to:

Zheng Cai, Alan L. Cox, T. S. Eugene Ng, "Maestro: Balancing Fairness, Latency and Throughput in the OpenFlow Control Plane", Rice University Technical Report TR11-07.
This work has also resulted in the following theses:

Zheng Cai, "Design and Implementation of the Maestro Network Control Platform", M.S. Thesis, Rice University, 2009. This primarily deals with the abstractions used in Maestro for application functionality composition and interaction.

Zheng Cai, "Maestro: Achieving Scalability and Coordination in Centralized Network Control Plane", Ph.D. Thesis, Rice University, 2011. This primarily deals with the scalability, performance, and applications of Maestro.

A related work leveraging Maestro as the control platform is:

Zheng Cai, Florin Dinu, Jie Zheng, Alan L. Cox, T. S. Eugene Ng, "CONTRACT: Incorporating Coordination into the IP Network Control Plane", IEEE ICDCS'10, Genoa, Italy, June 2010.
For discussions and questions, please join the Maestro Google group. If you cannot join the Google group, please contact Zheng Cai directly.

The Maestro project is supported by NSF's NeTS FIND Grant No. CNS-0721990.



Key people of the Maestro project: T. S. Eugene Ng (PI), Alan L. Cox (co-PI), Zheng Cai (code maintainer), Florin Dinu, Jie Zheng, all from the department of computer science of Rice University.
