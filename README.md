# openSUSE Tumbleweed (cpak)

## Installation

```bash
cpak install github.com/containerpak/opensuse
```

Create a persistent environment and open Bash:

```bash
cpak environment create --name openSUSE --origin github.com/containerpak/opensuse
cpak environment shell --environment openSUSE --command /bin/bash
```

The environment keeps its root filesystem and private home between sessions. It has network access for `zypper`; host files, desktop services and devices are not exposed by default.
