@def title = "ACEsuit"
@def subtitle = "A Julia Software Suite for ACE Modelling"
@def tags = ["syntax", "code"]


`ACEsuit` is a collection of Julia packages built around the *Atomic Cluster Expansion* (ACE) Model, an efficient parameterisation scheme for many-body interactions in particle systems. ACE models are defined in terms of body-ordered polynomial invariant features of (possibly decorated) point clouds.  This github org collects a wide variety of Julia and Python packages that build in some way on ACE methodology. 

### ACE Potentials in Julia

[`ACEpotentials.jl`](https://github.com/ACEsuit/ACEpotentials.jl) provides a user-oriented interface to a collection of several Julia packages that interoperate to fit models for atomic cluster expansion (ACE) interatomic potentials. 
* [github repo ACEpotentials.jl](https://github.com/ACEsuit/ACEpotentials.jl) : user-oriented interface codes, documentation source
* [documentation](https://acesuit.github.io/ACEpotentials.jl/dev/) : documentation pages
* [Discussion group](https://github.com/ACEsuit/ACEpotentials.jl/discussions) : discussion group


### MACE 

MACE provides fast and accurate machine learning interatomic potentials with higher order equivariant message passing. Each message uses a variant of the ACE expansion to make the higher body order computationally efficient. The [mace package](https://github.com/ACEsuit/mace) is implemented in PyTorch.


### Under Development

* [ACE.jl github repo](https://github.com/ACEsuit/ACE.jl) : an extension of `ACE1.jl` (on which `ACEpotentials.jl` builds) to allow equivariant features 
* [`ACEatoms.jl`](https://github.com/ACEsuit/ACEatoms.jl) - experimental interatomic potentials via `ACE.jl`
* [`ACEds.jl`](https://github.com/ACEsuit/ACEds.jl) - coarse-grained dynamical systems 
* `ACEhamiltonians.jl` : Hamiltonian operators with ACE, e.g., for tight binding 
* `ACEpsi.jl` : wave functions with ACE and VMC 
* `Polynomials4ML.jl` : new high-performance kernels for ACE models 
* `EquivariantModels.jl` : rewriting of ACE model architectures using `Lux.jl`
