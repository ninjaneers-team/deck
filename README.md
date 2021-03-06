# deck Helm Chart

[![Build Status](https://travis-ci.org/ninjaneers-team/deck.svg?branch=master)](https://travis-ci.org/ninjaneers-team/deck)

This is an implementation of deck batch job for kubernetes to migrate Open Policy Agent policies

## Pre Requisites
* Kubernetes 1.9+

## Chart Details
This chart will do the following:
* Start a job container as post-install step to migrate policies 

## Configuration

The chart can be customized using the following configurable parameters:

| Parameter                       | Description                                                     | Default                      |
| ------------------------------- | ----------------------------------------------------------------| -----------------------------|
| `image.repository`              | Container image name                                  | `ninjaneers/deck` |
| `image.tag`                     | Container image tag                                   | `latest`                    |
| `image.pullPolicy`              | Container pull policy                                 | `Always`                     |
| `imagepullSecret`              | Pod pull secret                                       | ``                     |
| `host`                  | Opa host url                                         | `http://localhost:8181`                  |
| `data`           | Opa.yaml configuration file        | `{}`                         |

Specify parameters using `--set key=value[,key=value]` argument to `helm install`

Alternatively a YAML file that specifies the values for the parameters can be provided like this:
