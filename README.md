

`ACEsuit` is a collection of Julia packages built around `ACE.jl` which provides a general and flexible implementation of the *Atomic Cluster Expansion* (ACE). ACE is an efficient parameterisation scheme for general permutation and isometry equi-variant functions. The focus of `ACEsuit` is on applications to modelling particle interactions. 

### Stable Version: ACE1.jl

* [github repo ACE1.jl](https://github.com/ACEsuit/ACE1.jl)
* [documentation](https://acesuit.github.io/ACE1docs.jl/dev/)
* [documentation repo](https://github.com/ACEsuit/ACE1docs.jl)
* [Discussion group](https://github.com/ACEsuit/ACE1docs.jl/discussions)
 
This is a stable package that was split off from the development version and will be maintained separately, maintaining strict semver backward compatibility and user-oriented documentation. `ACE1.jl` is limited to modelling interatomic potential interactions, or more generally *invariant* properties. Bugfixes and urgent features will continue to be included, but significant new development will more likely happen in the development version. 

See the [documentation](https://acesuit.github.io/ACE1docs.jl/dev/) for installation instructions and usage.

### Development Version: ACE.jl

* [ACE.jl github repo](https://github.com/ACEsuit/ACE.jl)
* [Developer docs](https://acesuit.github.io/ACE.jl/dev/)
* [Discussions](https://github.com/ACEsuit/ACE.jl/discussions)

`ACE.jl` is currently being [rewritten](https://github.com/ACEsuit/ACE.jl) to account for a variety of generalisations and new features, in particular equivariant properties and automatic differentiation. `ACE.jl` is entirely application agnostic and several wrapper packages are now being developed to enable different applications, mostly still experimental, including 

* [`ACEatoms.jl`](https://github.com/ACEsuit/ACEatoms.jl) - interatomic potentials 
* [`ACEflux.jl`](https://github.com/ACEsuit/ACEflux.jl) - nonlinear models
* [`ACEds.jl`](https://github.com/ACEsuit/ACEds.jl) - coarse-grained dynamical systems 
* `ACEhamiltonians.jl` - to be published soon

Please [join the ACE.jl discussions](https://github.com/ACEsuit/ACE.jl/discussions) if you have any informal questions about this package. 

### Tutorials

A simple tutorial on fitting an ACE using IPFitting on DFT Al data can be found [here](https://github.com/ACEsuit/acesuit.github.io/blob/main/tutorials/ACE%20Fitting.ipynb); or use the [nbviewer](https://nbviewer.jupyter.org/github/ACEsuit/acesuit.github.io/blob/main/tutorials/ACE%20Fitting.ipynb)

To use the ACE as a python ASE calculator please have a look [here](https://github.com/ACEsuit/acesuit.github.io/tree/main/tutorials/PyJuLIP_interface.ipynb) (requires pyjulia and [pyjulip](https://github.com/casv2/pyjulip) packages); or use the [nbviewer](https://nbviewer.jupyter.org/github/ACEsuit/acesuit.github.io/blob/main/tutorials/PyJuLIP_interface.ipynb)

These tutorials will move over to the ACE1docs repository.
