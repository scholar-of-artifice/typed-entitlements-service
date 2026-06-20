# Go to the project directory
We want this per project.
```
cd backend_service
```

# Get `ocamlformat`
Install `ocamlformat`:
```
opam install ocamlformat
```

# Make a file
Make and `ocamlformat` file:
```
echo "version = `ocamlformat --version`" > .ocamlformat
```