# AITW-JupyterLab Docker Extension

This is a Docker Extension aimed at facilitating the access of [AI-TranspWood](https://www.ai-transpwood-project.eu/) codebases made available in [EESSI](https://www.eessi.io/).
Each code base will present a notebook with an example on how to run a specific tool or workflow with a Graphical User Interface (GUI).

## Installation

### From Marketplace (not yet available)

> **NOTE**: The extension is not yet available in the Marketplace, but it will be [soon](https://github.com/docker/extensions-submissions/issues/224).

Since Docker Desktop [v4.11.0](https://docs.docker.com/desktop/release-notes/#docker-desktop-4110) the AITW-JupyterLab Extension is available in the Marketplace page:

- From the Docker Desktop main window click on the **Extensions** tab in left side menu.
- If you have not installed any extension yet, you will automatically jump to the **Manage**>**Browse** page
- If you have already installed some extension, just click on the **Manage** tab and then on **Browse** button at top right side of the window
- Look for **AITW-JupyterLab** extension (it will have the AITW project logo on the left)
- Click on install

### From command line

Since the extension is not yet available in the Marketplace, you will have to install it from the command line.
From Docker Desktop, you can open a terminal by clicking on the ">_ Terminal" button at the bottom right corner of the window.

**Note**: Since the extension is not yet distributed through the Marketplace, you will have to configure Dockere Desktop to allow installing extensions from non-official sources. To do that, go to **⚙️Settings** > **🧩Extensions** and untick the "Only allow extensions distributed through the Docker Marketplace" option.

Then run the following command in the terminal to install the extension:

```console
$ docker extension install aitranspwood/jupyter-docker-extension
Extensions can install binaries, invoke commands, access files on your machine and connect to remote URLs.
Are you sure you want to continue? [y/N] y
Extracting metadata and files for the extension "aitranspwood/jupyter-docker-extension:latest"
Installing service in Desktop VM...
Setting additional compose attributes
Installing Desktop extension UI for tab "AITW-JupyterLab"...
Extension UI tab "AITW-JupyterLab" added.
Starting service in Desktop VM......
Service in Desktop VM started
Extension "AI-TranspWood codebases in EESSI" installed successfully
```
**Note**: Docker Extension CLI is required to execute above command, that is normally included in Docker Desktop installation. If it does not work,follow the instructions at [Extension SDK (Beta) -> Prerequisites](https://docs.docker.com/desktop/extensions-sdk/#prerequisites) page for instructions on how to add it.
For more information, see the [Docker documentation](https://docs.docker.com/extensions/non-marketplace/).


## Notes

- The CVMFS cache is configured to use up to 10GB of disk space on your machine, this is not yet configurable so make sure you have enough disk space available (on average you will need ~3GB, when loading all examples).


## Usage

Once the extension is installed a new extension is listed in the Extension pane of Docker Desktop.
Click on the project icon, the JupyterLab welcome page will appear.
From there you check out the available demo notebooks under the "AITW" list.


## Persistent storage

Any data stored in the `/home/eessi-user` directory in the container will be persisted against Docker Desktop restarts or Extension updates.
The data from the CVMFS cache is also persisted to make running EESSI software quicker after restarts.


## Uninstall

### From Docker Desktop

- Navigate to the same **Extensions** > **Manage** page where you installed the extension.
- Click the three dots menu on the extension card and select **Uninstall**.

### From Command Line

```console
$ docker extension uninstall aitranspwood/jupyter-docker-extension
Extension "Jupyter Notebook" uninstalled successfully
```

## Sources

List of repositories hosting the source code used in this extension:

- Docker Extension: https://github.com/AI-TranspWood/jupyter-docker-extension
- EESSI-enabled JupyterLab container with preloaded AITW notebooks: https://github.com/AI-TranspWood/EESSI-jupyterlab-docker
- AITW notebooks: https://github.com/AI-TranspWood/jupyter-notebooks
