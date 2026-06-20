
## Navigate to the Project Directory
Go into `backend_service/` directory.
```
cd backend_service
```

## Create the Local Switch
Create an `opam` switch.
```
opam switch create .
```


## Activate the Switch
Run this command once per terminal session to make sure your terminal points to the local `_opam` switch.
```
eval $(opam env --switch=.)
```

## Install Dune
Make an `opam` file.
```
opam install dune
```

## Generate the OPAM file
Make an `opam` file.
```
dune build @opam
```

## Install Project Dependencies
Now that the `.opam` file exists, we can tell `opam` to install all the listed dependencies.
```
opam install . --deps-only --with-test --with-doc --with-dev-setup
```

## Compile
Compile the entire project.
```
dune build
```

## Run
Run the compiled binary. It usually lives somewhere like this:
```
dune exec ./_build/default/api_boundary_layer/main.exe 
```
