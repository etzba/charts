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
helm install image-updater image-updater/image-updater -n image-updater --create-namespace
```

### secret-distributor

To install secret-distributor in Kubernetes cluster:

```sh
helm install secret-distributor etzba/secret-distributor -n secret-distributor --create-namespace
```