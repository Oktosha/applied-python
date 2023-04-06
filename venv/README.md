# venv

`venv` stands for virtual environment. Virtual environments allow you to better track and manage dependencies for your python project.

## Creating venv

The command below creates a virtual environment with `python3` in the folder `awesome-env`

```bash
python3 -m venv awesome-env
```

Your environment can have any reasonable name (emoji and spaces inside the name are probably not the best idea, but any valid variable name in C should be good). I usually name the environment after the project I use it for.

Your environment can be located in any folder. Some people keep environments close to the projects that use them, some people keep all the virtual environments they use inside one folder in the home directory.

If you are going to place the virtual environment inside a git repo folder don't forget to add it to `.gitignore`.

You usually create the virtual environment for the project once. Then you activate it whenever you are working on the project and deactivate it when you're done.

## Activating and deactivating venv

The command below activates the virtual environment localed in the folder `awesome-env`

```bash
source awesome-env/bin/activate
```

After executing this command your prompt will change to show the name of the activated environment: from something like this `➜ current_dir` to `(awesome-env) ➜ current_dir`. Now your `python` command is the python from the virtual environment (and not python 2, for example).

To deactivate the current virtual environment, use the deactivate command

```bash
deactivate
```

You need to activate the virtual environment in every terminal session you want to use it. Activating a virtual environment in one tab of the terminal doesn't activate it in another tab. Closing tab with an active virtual environment doesn't deactivate the environment in other tabs. Deactivating a virtual environment in one tab of the terminal doesn't deactivate the environment in other tabs.

## Managing packages inside venv

The command below installs all the packages listed inside `requirements.txt` into current active python (have a look at an example requirements.txt inside this folder).

```bash
pip install -r requirements.txt
```

If the active python is the python from a virtual environment, it installs the requested packages inside the virtual environment folder. In current example they would be located somewhere inside `awesome-env/lib/python3.9/site-packages`.

You only have to install a package into environment once. After this you'll gain access to this package whenever you activate the environment where you've installed it.

You can have a look at the packages installed into an environment with the command `pip freeze` when the environment is activated.

```bash
pip freeze
```

That's exactly how you create `requirements.txt`

```bash
pip freeze > requirements.txt
```

You can install new packages into environment: use `pip install` while it is active. The command below will install the library `plumbum`.

```bash
pip install plumbum
```

You can uninstall packages as well. The command below will uninstall the library `plumbum`.

```bash
pip uninstall plumbum
```

Don't forget to keep your `requirements.txt` in sync with the actual packages installed into the virtual environment for your project.
