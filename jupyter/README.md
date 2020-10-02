## Installing jupyter lab
```
conda install -c conda-forge jupyterlab
```
## Installing jupyter notebook
```
conda install -c conda-forge notebook
```
## Installing voila
```
conda install -c conda-forge voila
```
## Installing ipywidgets
```
conda install -c conda-forge ipywidgets
```
## Insatalling jupyter lab extension
```
conda install -c conda-forge nodejs
```
```
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```
## Installing with multiple environment
```
conda install -n base -c conda-forge widgetsnbextension
conda install -n py36 -c conda-forge ipywidgets
```
## Installing with pip
```
pip install ipywidgets
jupyter nbextension enable --py widgetsnbextension
```
```
jupyter nbextension enable --py widgetsnbextension --sys-prefix
```

## How to run jupyter notebook in remote server and do the port forwarding in local machine

#### Step 1: Run Jupyter Notebook from remote machine
Log-in to your remote machine the usual way you do. In most cases, this is simply done via an ssh command. Once the console shows, type the following:
```
remoteuser@remotehost: jupyter notebook --no-browser --port=XXXX

# Note: Change XXXX to the port of your choice. Usually, the default is 8888. 
# You can try 8889 or 8890 as well.
```
- jupyter notebook: simply fires up your notebook
- --no-browser: this starts the notebook without opening a browser
- --port=XXXX: this sets the port for starting your notebook where the default is 8888. When it’s occupied, it finds the next available port.

#### Step 2: Forward port XXXX to YYYY and listen to it
In your remote, the notebook is now running at the port XXXX that you specified. What you’ll do next is forward this to port YYYY of your machine so that you can listen and run it from your browser. To achieve this, we write the following command:
```
localuser@localhost: ssh -N -f -L localhost:YYYY:localhost:XXXX remoteuser@remotehost
```
- `ssh`: your handy ssh command. See man page for more info
- -N: suppresses the execution of a remote command. Pretty much used in port forwarding.
- -f: this requests the ssh command to go to background before execution.
- -L: this argument requires an input in the form of local_socket:remote_socket. Here, we’re specifying our port as YYYY which will be binded to the port XXXX from your remote connection.

#### Step 3: Fire-up Jupyter Notebook
```
localhost:YYYY
```

#### Closing all connections
To close connections, I usually stop my notebook from remote via `CTRL + C` then `Y`, and kill the process on `YYYY` via:
```
localuser@localhost: sudo netstat -lpn |grep :YYYY

# This will show the process ID (PID), e.g. ABCDEF of the one running in YYYY,
# you can kill it by simply typing

localuser@localhost: kill ABCDEF
```
