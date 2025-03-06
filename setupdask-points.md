# We can setup / install dask in local (single machine or)
## Understanding Dask: Concepts Before Installation

Before installing Dask, let’s understand its key components:

### Dask Ecosystem

Dask has three main APIs:

- **Dask DataFrame** – Parallel processing for Pandas-like operations.
- **Dask Array** – Parallelized NumPy-like operations.
- **Dask Delayed & Futures** – General parallel task execution.

### Dask Execution Model

Dask has a lazy evaluation model like Spark:

- Tasks are scheduled first (DAG - Directed Acyclic Graph).
- Execution happens only when needed (when `.compute()` is called).

### Dask Deployment Modes

| Deployment Mode         | Usage Scenario                        |
|-------------------------|---------------------------------------|
| Single Machine (Local Mode) | Uses multiple CPU cores              |
| Distributed Cluster     | Scales to multiple nodes              |
| Kubernetes Deployment   | Runs in containerized environments    |
| Cloud (AWS, Azure, GCP) | Uses cloud-based Dask clusters        |

## Installing Dask on a Local System

Dask runs efficiently on a single machine using multiple CPU cores.

### Installing Dask (Basic)

Use `pip` to install the basic version:

```bash
pip install dask
```

OR for the full Dask ecosystem:

```bash
pip install "dask[complete]"
```

### Verifying Installation

Run Python and check:

```python
import dask
print(dask.__version__)
```

### Running Dask in Local Mode

Dask automatically runs in multi-threaded mode. You can explicitly set single-machine mode:

```python
from dask.distributed import Client

client = Client()  # Uses all available CPU cores
print(client)
```

This will output details about available workers and memory usage.

## Running Dask in a Distributed Environment

To scale Dask beyond a single machine, you need a distributed cluster.

### Setting Up a Distributed Dask Cluster

Dask uses a scheduler-worker architecture:

- **Scheduler**: Assigns tasks to workers.
- **Workers**: Execute computations in parallel.
- **Client**: Interface to interact with the cluster.

#### Installing Dask Distributed

```bash
pip install "dask[distributed]"
```

#### Running Dask Scheduler & Workers

Start the scheduler:

```bash
dask-scheduler
```

Start workers (on different machines if needed):

```bash
dask-worker tcp://<SCHEDULER-IP>:8786
```

Now, connect using Python:

```python
from dask.distributed import Client
client = Client("tcp://<SCHEDULER-IP>:8786")
print(client)
```

#### Scaling Workers Dynamically

You can add more workers on demand:

```python
client.scale(4)  # Scale to 4 workers
```