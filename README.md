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

# cd and update the pyproject.toml config so the name of your package is correct
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
# create a virtual venv if you haven't already
python3 -m venv ~/path/to/virtualenvs/my_new_python_project
source ~/path/to/virtualenvs/my_new_python_project/bin/activate

# make sure you can run the main script
python3 main.py
```

## Updating Python Dependencies

After running `nix develop` simply run go into `flake.nix` and add your
dependency to the list of existing dependencies, which will be next to the
`with pkgs.python311Packages;` text inside of `flake.nix`. Then exit out of your
Nix dev shell using `exit` followed by `nix develop` and Nix will take care of
pulling in the correct dependencies
