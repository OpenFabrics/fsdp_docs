# Build Server Instructions

## Running containers
The containers for Fedora-based images are maintained by the [cki-project](https://gitlab.com/cki-project/containers).
Instructions for accessing and running these images using rootless `podman` can be found below.
### builder-fedora (Fedora 33)
Run the following command:

`podman run -it registry.gitlab.com/cki-project/containers/builder-fedora`

You should now be running the container image from the registry.

### builder-rawhide (Fedora 34)
Run the following command:

`podman run -it registry.gitlab.com/cki-project/containers/builder-rawhide`

You should now be running the container image from the registry.


### builder-rhel7
TBA
### builder-rhel8
TBA
### builder-rhel9
TBA 

