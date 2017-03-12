# PiHole Helm Chart

* Installs the web dashboarding system [PiHole](https://pi-hole.net/)

## TL;DR;

```console
$ helm install incubator/pihole
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm repo add incubator http://storage.googleapis.com/kubernetes-charts-incubator
$ helm install --name my-release incubator/pihole
```

## Uninstalling the Chart

To uninstall/delete the my-release deployment:

```console
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.


## Configuration

| Parameter                             | Description                         | Default                                           |
|---------------------------------------|-------------------------------------|---------------------------------------------------|
| `server.ip`                           | Container image to run              | diginc/pi-hole:arm                                |
| `service.externalPort`                | External port for the web UI        | 9180                                              |
| `resources`                           | Server resource requests and limits | requests: {cpu: 100m, memory: 128Mi}              |
