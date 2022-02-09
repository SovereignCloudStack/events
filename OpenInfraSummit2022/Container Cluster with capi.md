# Flexible container management with cluster-API on OpenStack

Track: Container Infrastructure

Authors: Matt Pryor, Kurt Garloff

## Abstract (1000 chars)

OpenStack has had the ability to manage container orchestration engines with
magnum for a long time. This presentation however will show how to manage
kubernetes(k8s) clusters on OpenStack the k8s declarative way, using the k8s
cluster API and its OpenStack provider.

It will show how to bootstrap the initial k8s cluster for hosting the
cluster-api (capi) and openstack provider (capo) pods.

The fresh setup can be used to create workload clusters and deploy some
standard services into them such as the OpenStack Cloud Controller Manager
(OCCM), the cinder CSI storage driver and a CNI provider. The size of the
running clusters can be adjusted and rolling upgrades be performed using new
machine images and even k8s versions.

Finally the presenters cover a set of helm charts that help with automating
such upgrades and also provide a flexible way to inject a set of standard
services into the workload clusters.

## Social summary (100 chars)

Using the OpenStack cluster API provider to flexibly create and manage k8s
clusters on OpenStack platforms.

## What should attendees expect to learn? (1000 chars)

Attendees will get an introduction to the concepts behind k8s cluster API and
learn how to bootstrap a management node that runs a k8s cluster with cluster
API and the OpenStack cluster API provider installed. The authors will use the
terraform automation built in the Sovereign Cloud Stack project which bootraps
a cluster using kind and cover some of the challenges like adjusting MTU or
passing in credentials for interfacing OpenStack.

They will learn how workload clusters can be configured and created and
adjusted on the fly using the cluster API interfaces.

Upgrading machine descriptions requires rotating the templates which can become
tedious. Attendees will get an introduction to the helm charts that help
automating the rotation of machine templates.

The authors will also share some of their experience managing k8s cluster on
top of the SCS and StackHPC OpenStack platforms.

## Additional resources

[1] https://github.com/SovereignCloudStack/k8s-cluster-api-provider/
[2] https://github.com/stackhpc/capi-helm-charts
