

`ACEsuit` is a collection of Julia modules built around `ACE.jl` which provides a general and flexible implementation of the *Atomic Cluster Expansion* (ACE). ACE is an efficient approximation scheme for general permutation and isometry equi-variant functions. The focus of `ACEsuit` is on applications to modelling particle interactions. It provides constructions of symmetric polynomial bases.

`ACE.jl` is currently being [rewritten](https://github.com/ACEsuit/ACE.jl) to account for a variety of generalisations. In the meantime `v0.8.x` provides a relatively [stable version](https://github.com/ACEsuit/ACE.jl/tree/dev-v0.8.x) which is limited to modelling interatomic potential interactions (or more generally *invariant* properties).

### Links

* [ACE.jl Stable](https://github.com/ACEsuit/ACE.jl/tree/dev-v0.8.x) (includes a basic documentation in README + examples)
* [ACE.jl Development](https://github.com/ACEsuit/ACE.jl) (under heavy development) [[docs]](https://acesuit.github.io/ACE.jl/dev/)

### Installation (v0.8.x) --- Short Version

```julia
using Pkg; pkg"registry add https://github.com/JuliaMolSim/MolSim.git"; pkg"add JuLIP ACE PyCall ASE IPFitting"
```

### Installation (v0.8.x)

If you have any difficulties with this setup process, please file an issue.

1. Install [Julia](https://julialang.org). We recommend v1.6 or upwards, but v1.3 upwards should in principle work as well.
2. Install the [`MolSim` registry](https://github.com/JuliaMolSim/MolSim); from the Julia REPL, switch to package manager `]` and then run
```julia
registry add https://github.com/JuliaMolSim/MolSim.git
```
3. Install some important registered packages; from Julia REPL / package manager:
```julia
add JuLIP ACE         # maybe add other packages from MolSim registry
```
This will install the *stable* `v0.8.x` version of ACE, as the (equivariant) development version has not been registered yet.
4. To use [ase](https://wiki.fysik.dtu.dk/ase/) from Julia, you can use [PyCall](https://github.com/JuliaPy/PyCall.jl) or the [ASE.jl](https://github.com/JuliaMolSim/ASE.jl) interface. To install these, run
```julia
add PyCall ASE
```
from the package manager.
5. For fitting, you may wish to use [`IPFitting.jl`](https://github.com/cortner/IPFitting.jl),
```julia
add IPFitting
```
This has `ASE.jl` as a dependency. (Keep fingers crossed and hope it will be compatible with the current version of `ACE.jl`...)

### Tutorials

A simple tutorial on fitting an ACE using IPFitting on DFT Al data can be found here
To use the ACE as a python ASE calculator please have a look here (requires pyjulia and pyjulip packages)

### Trouble-shooting

* On some systems `ASE.jl` is unable to automatically install python dependencies. We found that installing [Anaconda](https://anaconda.org) and then pointing `PyCall.jl` to the Anaconda installation (cf [PyCall Readme](https://github.com/JuliaPy/PyCall.jl)) resolves this. After installing Anaconda, it should then be sufficient to build `ASE.jl` again.
* If you cannot use Anaconda python, or if the last point failed, then you can try to install the python dependencies manually before trying to build `ASE.jl` again. Specifically, it should be sufficient to just install the [ase](https://wiki.fysik.dtu.dk/ase/) package. Please follow the installation instructions on their website.
