## About

The AWS Neuron device plugin for Kubernetes is a Daemonset that allows you to automatically:

* Expose the number of Neuron devices on each nodes of your cluster
* Run Neuron enabled containers in your Kubernetes cluster.


This repository contains AWS Neuron K8's official implementation of the [Kubernetes device plugin](https://awsdocs-neuron.readthedocs-hosted.com/en/latest/release-notes/neuron-k8.html).


## Prerequisites

* Node running Amazon EKS optimized accelerated Amazon Linux AMI

## Installation

This chart is listed on https://artifacthub.io/packages/helm/julian3xl/aws-neuron-device-plugin

## Issues

Bootstraping on the Amazon EKS optimized accelerated Amazon Linux AMIs has a bug that tries to find nvidia devices and fails in the case of none nvidia devices found. To fix that you have to remove the nvidia-smi binary before calling the bootstrap script.
