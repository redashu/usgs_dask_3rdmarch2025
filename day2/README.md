### Revision 

### World of Horizental scaling 

<img src="scale1.png">

### Dask 

<img src="dask1.png">

### More dask info 

<img src="dask2.png">

### aws cloud services 

<img src="aws1.png">

### Understanding Dask Cluster 

<img src="daskcls1.png">

### Dask Cluster Components 

<img src="daskcls2.png">

## dask Client info 

<img src="daskcls3.png">

### Verify Dask client details 

```
ubuntu@dask-client:~$ pip -V
pip 24.0 from /usr/lib/python3/dist-packages/pip (python 3.12)
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ uname 
Linux
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ python3 -V
Python 3.12.3
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ pip -V
pip 24.0 from /usr/lib/python3/dist-packages/pip (python 3.12)
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ pip  list  | grep -i numpy 
ubuntu@dask-client:~$ 
ubuntu@dask-client:~$ ls
client  jupyterhub.sqlite  jupyterhub_config.py.backup  jupyterhub_cookie_secret
ubuntu@dask-client:~$ source client/bin/activate
(client) ubuntu@dask-client:~$ 
(client) ubuntu@dask-client:~$ pip  list  | grep -i numpy 
numpy                     2.2.3
(client) ubuntu@dask-client:~$ pip  list  | grep -i pandas
pandas                    2.2.3
(client) ubuntu@dask-client:~$ pip  list  | grep -i dask
dask                      2025.2.0
dask_labextension         7.0.0
(client) ubuntu@dask-client:~$ pip  list  | grep -i distri
distributed               2025.2.0
(client) ubuntu@dask-client:~$ 

```