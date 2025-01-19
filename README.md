# sinteractive

`sinteractive` is a small wrapper that  submits a sbatch job to slurm to start a GNU screen session on a
compute node. It will wait until the job starts and then SSH to the compute
node attached to the screen session that was started. This creates a detachable
interactive shell session as well as allowing X forwarding to work.

You can specify any valid sbatch options as necessary.

There is one non-slurm option: `--port '<port number>'`, for propoer port forwarding. By default, `sinteractive` will use the port specified by the variable `$ANVIO_PORT`.
