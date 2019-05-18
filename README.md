# kubewatch

Kubernetes CLI plugin for better resource watching output.

![alt text](./kubewatch.gif)

## Installation

```bash
git clone https://github.com/lee0c/kubewatch.git
cd kubewatch
chmod +x kubewatch
ln -s /path/to/kubewatch/kubewatch /usr/local/bin/kubewatch
```

To use this as a [kubectl plugin](https://kubernetes.io/docs/tasks/extend-kubectl/kubectl-plugins/) (recommended), change the last command:

```bash
ln -s /path/to/kubewatch/kubewatch /usr/local/bin/kubectl-watch
```

You can then run `kubectl plugin list` to see all available plugins, and use `kubectl watch ---` as a kubectl command.

## Use

`kubectl watch` will take any arguments `kubectl get` takes. It additionally adds a few options which **must be specified before any standard kubectl arguments**. Arguments that require values are shown with their default value.

| Options |  |
| :------ | --- |
| -c, --calls 60 | Make 60 calls before exiting (pass 0 to disable progress bar/exiting) |
| -s, --sleep 1 | Sleep for the specified number of seconds between calls |
| -h, --help | Displays help text. |