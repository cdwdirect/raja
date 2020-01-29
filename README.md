
[comment]: # (#################################################################)
[comment]: # (Copyright 2016-19, Lawrence Livermore National Security, LLC)
[comment]: # (and RAJA project contributors. See the RAJA/COPYRIGHT file)
[comment]: # (for details.)
[comment]: # 
[comment]: # (# SPDX-License-Identifier: BSD-3-Clause)
[comment]: # (#################################################################)

# <img src="/share/raja/logo/RAJA_LOGO_Color.png?raw=true" width="128" valign="middle" alt="RAJA"/>

[![Build Status](https://travis-ci.org/LLNL/RAJA.svg?branch=develop)](https://travis-ci.org/LLNL/RAJA)
[![Join the chat at https://gitter.im/llnl/raja](https://badges.gitter.im/llnl/raja.svg)](https://gitter.im/llnl/raja?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Coverage](https://img.shields.io/codecov/c/github/LLNL/RAJA/develop.svg)](https://codecov.io/gh/LLNL/RAJA)

RAJA is a collection of C++ software abstractions, being developed at
Lawrence Livermore National Laboratory (LLNL), that enable architecture
portability for HPC applications. The overarching goals of RAJA are to:

  * Make existing (production) applications *portable with minimal disruption*
  * Provide a model for new applications so that they are portable from
    inception.

RAJA uses standard C++11 -- C++ is the predominant programming language in
which many LLNL codes are written. RAJA is rooted in a perspective based on 
substantial experience working on production mesh-based multiphysics 
applications at LLNL. Another goal of RAJA is to enable application developers
to adapt RAJA concepts and specialize them for different code implementation 
patterns and C++ usage, since data structures and algorithms vary widely 
across applications.

RAJA shares goals and concepts found in
other C++ portability abstraction approaches, such as
[Kokkos](https://github.com/kokkos/kokkos)
and [Thrust](https://developer.nvidia.com/thrust). 
However, it includes concepts that are absent in other models and which are 
fundamental to LLNL codes. 

It is important to note that RAJA is very much a work-in-progress.
The community of researchers and application developers at LLNL that are
actively contributing to it and developing new capabilities is growing.
The publicly-released version contains only core pieces of RAJA as they
exist today. While the basic interfaces are fairly stable, the implementation
of the underlying concepts is being refined. Additional features will appear
in future releases.

Quick Start
-----------

The RAJA code lives in a GitHub [repository](https://github.com/llnl/raja).
To clone the repo, use the command:

    git clone --recursive https://github.com/llnl/raja.git

Then, you can build RAJA like any other CMake project, provided you have a C++
compiler that supports the C++11 standard. The simplest way to build the code,
using your system default compiler, is to run the following sequence of 
commands in the top-level RAJA directory (in-source builds are not allowed!):

    mkdir build
    cd build
    cmake ../
    make

More details about RAJA configuration options are located in the User 
Documentation.

We also maintain a [**RAJA Template Project**](https://github.com/LLNL/RAJA-project-template) that shows how to use RAJA in a CMake project, either as a Git
submodule or as an installed library.

User Documentation
-------------------

The [**RAJA User Guide and Tutorial**](http://raja.readthedocs.io/en/master/) 
is the best place to start learning about RAJA and how to use it.

To cite RAJA, please use the following references:

* RAJA Performance Portability Layer. https://github.com/LLNL/RAJA

* D. A. Beckingsale, J. Burmark, R. Hornung, H. Jones, W. Killian, A. J. Kunen, O. Pearce, P. Robinson, B. S. Ryujin, T. R. W. Scogland, "RAJA: Porrtable Performance for Large-Scale Scientific Applications", 2019 IEEE/ACM International Workshop on Performance, Portability and Productivity in HPC (P3HPC). [Download here](https://conferences.computer.org/sc19w/2019/#!/toc/14)

Related Software
--------------------

The [**RAJA Performance Suite**](https://github.com/LLNL/RAJAPerf) contains
a collection of loop kernels implemented in multiple RAJA and non-RAJA
variants. We use it to monitor and assess RAJA performance on different
platforms using a variety of compilers.

The [**RAJA Proxies**](https://github.com/LLNL/RAJAProxies) repository 
contains RAJA versions of several important HPC proxy applications.

[**CHAI**](https://github.com/LLNL/CHAI) provides a managed array abstraction
that works with RAJA to automatically copy data used in RAJA kernels to the
appropriate space for execution. It was developed as a complement to RAJA.

Mailing List
-----------------

Interested in keeping up with RAJA or communicating with its developers and
users? Please join our mailing list at Google Groups:
- [RAJA Google Group](https://groups.google.com/forum/#!forum/raja-users)

If you have questions, find a bug, or have ideas about expanding the
functionality or applicability of RAJA and are interested in contributing
to its development, please do not hesitate to contact us. We are very
interested in improving RAJA and exploring new ways to use it.

Contributions
---------------

The RAJA team follows the [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/) development model. Folks wishing to contribute to RAJA, should
include their work in a feature branch created from the RAJA `develop` branch.
Then, create a pull request with the `develop` branch as the destination. That
branch contains the latest work in RAJA. Periodically, we will merge the 
develop branch into the `master` branch and tag a new release.

Authors
-----------

The original developers of RAJA are:

  * Rich Hornung (hornung1@llnl.gov)
  * Jeff Keasler (keasler1@llnl.gov)

Please see the [RAJA Contributors Page](https://github.com/LLNL/RAJA/graphs/contributors), to see the full list of contributors to the project.


License
-----------

RAJA is licensed under the BSD 3-Clause license,
(BSD-3-Clause or https://opensource.org/licenses/BSD-3-Clause).

Copyrights and patents in the RAJA project are retained by contributors.
No copyright assignment is required to contribute to RAJA.

Unlimited Open Source - BSD 3-clause Distribution
`LLNL-CODE-689114`  `OCEC-16-063`

For release details and restrictions, please see the information in the
following:
- [RELEASE](./RELEASE)
- [LICENSE](./LICENSE)
- [NOTICE](./NOTICE)


SPDX usage
------------

Individual files contain SPDX tags instead of the full license text.
This enables machine processing of license information based on the SPDX
License Identifiers that are available here: https://spdx.org/licenses/

Files that are licensed as BSD 3-Clause contain the following
text in the license header:

    SPDX-License-Identifier: (BSD-3-Clause)

External Packages
-------------------
RAJA bundles its external dependencies as submodules in the git repository.
These packages are covered by various permissive licenses.  A summary listing
follows. See the license included with each package for full details.

PackageName: BLT  
PackageHomePage: https://github.com/LLNL/blt
PackageLicenseDeclared: BSD-3-Clause

PackageName: camp
PackageHomePage: https://github.com/LLNL/camp
PackageLicenseDeclared: BSD-3-Clause

PackageName: CUB  
PackageHomePage: https://github.com/NVlabs/cub
PackageLicenseDeclared: BSD-3-Clause
