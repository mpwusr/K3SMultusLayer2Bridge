# K3s + Multus + Layer 2 Network Demo

This repo demonstrates how to configure Multus CNI on Rancher K3s with multiple Layer 2 bridge networks.

## Components

- `Multus` installed as a secondary CNI
- Two bridge interfaces: `br0` and `br1`
- Static IP assignment via Multus
- Demo pod with two interfaces using both bridges

## Usage

```bash
kubectl apply -f 00-multus-daemonset.yaml
kubectl apply -f 01-bridge-setup-daemonset.yaml
kubectl apply -f 02-net-attach-defs.yaml
kubectl apply -f 03-demo-pod.yaml
