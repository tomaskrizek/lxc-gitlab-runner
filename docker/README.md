# Container images with systemd

## Why?

As a lightweight alternative to VMs. Systemd is necessary for some integration
/ packaging tests utilized by Knot Resolver.

## Building

To avoid copying common files, they are placed directly in `docker/` directory.
Consequently, it needs to be used as the context directory for the build.

```
# PWD => docker/

podman build -t registry.nic.cz/labs/lxc-gitlab-runner/debian/buster -f debian/buster .
```