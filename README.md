# Melville's Python Dev Environment Flake

A right and proper simple Flake for all your Python v3 needs. The world is your
burrito 🌯

## Why Does This Exist?

To make it easy to get started with Python.

## Cloning The Repo

Use these instructions to initialize a new git repository named
`my_new_python_project` using this flake as a template. Note, you must have
already created the `my_new_python_project` repo on GitHub

```bash
# clone existing repo
git clone git@github.com:Melvillian/python_devenv_flake.git my_new_python_project

# cd and update the Poetry config
cd my_new_python_project
sed -i '' 's/python_devenv_flake/my_new_python_project/g' pyproject.toml
mv python_devenv_flake my_new_python_project
git add .
git commit

# update the remote origin on GitHub
git remote add origin git@github.com:<YOUR_USERNAME>/my_new_python_project.git
git push -u origin main

# Done!
```

## Getting Started

```bash
nix develop
poetry install
poetry run main # executes the main script set in the pyproject.toml
```

## Updating Poetry Dependencies

After running `nix develop` simply run

`poetry add <YOUR_PYTHON_DEP>`

## TODO

- [ ] Get this working fresh multiple times
