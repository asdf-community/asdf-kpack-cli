# ASDF kpack-cli

[kpack-cli](https://github.com/vmware-tanzu/kpack-cli) plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

Heavily forked/copied from [asdf-kubectl](https://github.com/asdf-community/asdf-kubectl). Many thanks to all the contributors on that project.

## Installation

```
asdf plugin-add kpack-cli https://github.com/mindovermiles262/asdf-kpack-cli.git
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of kpack-cli

```
$ asdf install kpack-cli 0.9.1
[*] Downloading kpack from https://github.com/vmware-tanzu/kpack-cli/releases/download/v0.9.1/kp-darwin-amd64-0.9.1
[*] kpack-cli has been installed. Use 'kpack' to get started

$ asdf global kpack-cli 0.9.1
$ kpack
kp controls the kpack installation on Kubernetes.

kpack extends Kubernetes and utilizes unprivileged kubernetes primitives to provide
builds of OCI images as a platform implementation of Cloud Native Buildpacks (CNB).
Learn more about kpack @ https://github.com/pivotal/kpack
 
```

## Architecture Override

The `ASDF_KPACKCLI_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which kpack-cli build to download.

## Known Bugs

* kpack-cli versions before 0.7.0 do not download or install due to a change in the URL formatting of the github releases. If you need version 0.7.0 or before you should manually download and install the binaries from the [kpack-cli github releases page](https://github.com/vmware-tanzu/kpack-cli/releases)
