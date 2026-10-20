<p align="center">
  <img src="etzba.png" alt="etzba"/>
</p>

# charts

In this repository you'll find etzba helm charts, to deploy in your kubernetes cluster. To read more about etzba tools, go to https://etzba.com.

For every chart there is a dedicated section with the relevant command to install the chart.

### Add repositories

To add all helm repositories of etzba:

```sh
helm repo add etzba https://raw.githubusercontent.com/etzba/charts/master/
helm repo update
helm repo list
```

### image-updater

To install image-updater in Kubernetes cluster:

```sh
helm install image-updater etzba/image-updater -n image-updater --create-namespace
```

### secret-distributor

To install secret-distributor in Kubernetes cluster:

```sh
helm install secret-distributor etzba/secret-distributor -n secret-distributor --create-namespace
```

### etz

To install etz job in Kubernetes cluster (Use `--set` to configure several values like `etz.executionType` and `etz.commandArgs`):

```sh
helm install etz etzba/etz -n etz --create-namespace --set etz.executionType=api --set etz.commandArgs[0]="--url=https://etzba.com" --set etz.commandArgs[1]="--method=GET" --set etz.commandArgs[2]="-r=2" --set etz.commandArgs[3]="-d=30s"
```

```sh
helm install etz etzba/etz -n etz --create-namespace --set etz.executionType=api --set "etz.commandArgs={--url=https://etzba.com,--method=GET",-r=2,-d=30s}"
```

Go to the `values.yaml` file in etz chart to read more about how to `--set` the values and how to add it in order for the command to succeed.

Read more about how to use `etz` cli tool to understand better which values should be added and how to set a config file at https://etzba.com.
