Work in Progress !!!

== What is this ? ==

This is a big project about the PoC of an infrastructure related to cloud-native applications. It is a prelude of other projects, it has been made to demonstrate what i can achieve to learn by myself and to illustrate my skills in my resume. It's a prelude and prototype of other cool projects that have yet to come :) !

It is temporary public because i'm searching for an internship/job and i'm candidating to MsCs for the next year.

----------------------------------------------------------------------------------------------------

Kubernetes OS for Master Node (Configuration Rpm-Ostree)

This is the repo for the custom OS that i created for the SaaS project.
This image is not ready to use for development or production purposes it's 
a work in progress that will be customized.

The idea here is that we input to our Kubernetes OS, PKI and kubeconfigs files and our cluster
goes in the desired state.

It uses SystemD (services, path and target units) to get to the desired state progressively

multi-user.target -> etcd-ready.target -> kubernetes-ready.target -> gitlab-running.target (basically)

On the air updates are activated but it's not working because i intend to implement a Continuous Integration chain where it'll be done automatically, and i'm working heavily on some particular things right now to get a PoC running fast.

It needs some work (SELinux Up and Running, RPM creation and distrib repo management, Updates ; it's WIP)

Repo for the Super-Admin IaC is there : https://github.com/Xfireball8/AWSSuperAdminCode
Repo for the DevOps Engineer IaC is there : https://github.com/Xfireball8/SaasProjectCluster
