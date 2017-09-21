# Drone

[Drone](http://docs.drone.io/) is a lightweight, powerful continuous delivery platform built on Docker, written in Go.

## TL;DR;

```console
$ helm install stable/drone --set a=b,c=d
```

## Introduction

This chart creates a Drone deployment on a Kubernetes cluster using the Helm package manager.

The most basic setup includes:

- A [Drone Server](http://docs.drone.io/installation/) Pod
- A [Drone Agent](http://docs.drone.io/installation/) Pod

## Prerequisites

- Kubernetes 1.5+
- The ability to point a DNS entry or URL at your Drone installation

## Installing the Chart

To install the chart with the release name `my-drone`:

```bash
$ helm install stable/drone --name my-drone --set a=b,c=d
```

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-drone` deployment:

```console
$ helm delete my-drone
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

Please refer to [values.yaml](values.yaml) for the full run-down on defaults. These are a mixture of Kubernetes and drone directives.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

Alternatively, a YAML file that specifies the values for the parameters can be provided while
installing the chart using the `-f` flag. For example,

```bash
$ helm inspect values stable/drone > values.yaml
$ $EDITOR values.yaml # make some changes
$ helm install --name my-drone -f values.yaml stable/drone
```

## Documentation

- [Generic Drone installation instructions](http://docs.drone.io/installation/)
- [Drone usage instructions](http://docs.drone.io/getting-started/)
- [Drone plugin reference](http://docs.drone.io/plugin-overview/)
- [Drone CLI reference](http://docs.drone.io/cli-installation/)
