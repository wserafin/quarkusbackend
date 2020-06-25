# Edit in CodeReady Workspaces

We use Red Hat's Code Ready Workspaces (CRW) for application development. Pressing on the badge here will set up a workspace for you. 
You don't have to install anything on your workstation. CRW provides IDE and Runtimes!!

To start your workstation in Red Hat CodeReady Workspaces:
<a href="https://codeready-crw2.apps.ocp4.home.ocpcloud.com/f?url=https://github.com/wserafin/quarkusbackend">
    <img src="https://pbs.twimg.com/profile_images/700361197112000513/w9Cyilbf_400x400.png" width="130" alt="Push" align="top">
</a>

# runtime-quarkus

Created by the Cloud App Generator

Now that the application has been generated it can be deployed in the currently active project on OpenShift by going into the
project folder and running:

```
$ ./gap deploy
```

Now the only thing that is left to do is push the project's code to OpenShift to be run. There are two ways of doing that,
one is by first building the project yourself locally and pushing the resulting binary, like this:

```
$ ./gap build
$ ./gap push --binary
```

In most cases you can leave out the `--binary` flag because that's the default if a binary is available. In case you want
to push the sources and have the project be built on OpenShift you can do the following:

```
$ ./gap push --source
```

This is also the default when no binary is available and you omit the `--source` flag.

Building
=========

The application can be built by running:

```bash
$ mvn clean package
```
