When coding defensively, we treat warnings as errors.
Here is how we do that in `dune` projects.

```dune
(env
 (_
  (flags
   (:standard -w +A -warn-error +A))))
```
# What does this mean?

`_` a wildcard which means any environment (build, release, etc)
`:standard` inherits Dune's default compiler flags.
`-w +A` turn on all possible OCaml warnings.
`-warn-error +A` treat all warnings as compilation errors.

# Apply Autoformatting
```
dune build @fmt --auto-promote
```
