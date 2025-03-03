# Python to Spark 

![Data Processing](data1.png)

### To Do Fast Processing of Data 

![DDF](ddf.png)

### Python to Spark - to Dask 

![Dask](dask1.png)

# Dask Info 

Dask is a flexible, open-source library for parallel computing in Python. It is designed to scale Python code from single machines to large clusters, enabling efficient handling of larger-than-memory datasets and parallelizing computations. Dask integrates seamlessly with the Python ecosystem, including libraries like NumPy, pandas, and scikit-learn.

## Key Features

- **Parallel Computing**: Dask breaks down large computations into smaller tasks and executes them in parallel, leveraging multi-core CPUs or distributed clusters.
- **Scalability**: Works on a single machine or scales to thousands of nodes in a distributed cluster.
- **Familiar APIs**: Provides APIs that mimic popular libraries like:
    - `dask.array` for NumPy-like arrays.
    - `dask.dataframe` for pandas-like DataFrames.
    - `dask.bag` for processing semi-structured data (like JSON).
    - `dask.delayed` for custom parallel workflows.
- **Lazy Evaluation**: Computations are not executed immediately but are instead built into a task graph, which is optimized and executed later.
- **Out-of-Core Computation**: Handles datasets larger than memory by efficiently streaming data from disk.
- **Integration**: Works well with other Python libraries like NumPy, pandas, scikit-learn, and XGBoost.

## When to Use Dask?

- Your dataset is too large to fit into memory.
- You need to parallelize computations across multiple cores or machines.
- You want to scale pandas, NumPy, or custom Python workflows without rewriting code.
- You’re working with distributed systems or clusters (e.g., Kubernetes, Hadoop, or cloud environments).

## Core Components

- **Dask Scheduler**: Coordinates tasks across workers.
- **Dask Workers**: Execute tasks in parallel.
- **Dask Client**: Interface for users to interact with the scheduler and workers.
- **Task Graph**: A directed acyclic graph (DAG) that represents the computation.

## Example Use Cases

- **Large-Scale Data Analysis**: Process terabytes of data using `dask.dataframe`.
- **Machine Learning**: Scale scikit-learn workflows with `dask_ml`.
- **Custom Workflows**: Use `dask.delayed` to parallelize custom Python functions.
- **Distributed Computing**: Run computations on clusters using Dask’s distributed scheduler.

# Lab connect using SSH 

### ssh 

```sh
 ssh  ubuntu@34.30.215.102
The authenticity of host '34.30.215.102 (34.30.215.102)' can't be established.
ED25519 key fingerprint is SHA256:RidE6RR6bC2KKRWUdCXYgmtRn2MavPwP8cJ9fCkhAhk.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '34.30.215.102' (ED25519) to the list of known hosts.
ubuntu@34.30.215.102's password:
Welcome to Ubuntu 22.04.5 LTS (GNU/Linux 6.8.0-1021-gcp x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Mon Mar  3 17:53:52 UTC 2025

```
### setup of dask in single machine 

```
 python3 -m venv  ashu-env 
ubuntu@daskserver2:~$ ls
ashu-env
ubuntu@daskserver2:~$ 
```

### Installing dask basic and full both 

```
 9  source  ashu-env/bin/activate
   10  pip install numpy 
   11  pip install pandas
   12  history 
   13  pip install dask  # basic dask version 
   14  history 
   15  pip install "dask[complete]"  # full Dask ecosystem
```
