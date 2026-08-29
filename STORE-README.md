# Use openSUSE Tumbleweed as a persistent environment

Install the package once:

```bash
cpak install github.com/containerpak/opensuse
```

Create an environment and open Bash:

```bash
cpak environment create --name openSUSE --origin github.com/containerpak/opensuse
cpak environment shell --environment openSUSE --command /bin/bash
```

The shell runs as root inside the environment, so openSUSE packages can be installed normally:

```bash
zypper refresh
zypper install git gcc make
```

## Persistent storage

Installed packages, system configuration and the private home directory remain available after the shell closes or the environment stops. Host files, desktop services and devices stay unavailable unless you grant them through the environment settings.

## Manage the environment

```bash
cpak environment list
cpak environment inspect --environment openSUSE
cpak environment processes --environment openSUSE
cpak environment stop --environment openSUSE
```

Deleting the environment also deletes its installed packages, system changes and private home:

```bash
cpak environment delete --environment openSUSE
```
