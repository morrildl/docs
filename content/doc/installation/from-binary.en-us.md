---
date: "2016-12-01T16:00:00+02:00"
title: "Installation from binary"
slug: "install-from-binary"
weight: 10
toc: true
draft: false
menu:
  sidebar:
    parent: "installation"
    name: "From binary"
    weight: 20
    identifier: "install-from-binary"
---

# Installation from binary

All downloads come with SQLite, MySQL and PostgreSQL support, and are built with embedded assets. Keep in mind that this can be different for older releases. The installation based on our binaries is quite simple, just choose the file matching your platform from the [downloads page](https://dl.gitea.io/gitea), copy the URL and replace the URL within the commands below:

```
wget -O gitea https://dl.gitea.io/gitea/1.0.1/gitea-1.0.1-linux-amd64
chmod +x gitea
```

## Test

After following the steps above you will have a `gitea` binary within your working directory, first you can test it if it works like expected and afterwards you can copy it to the destination where you want to store it. When you launch Gitea manually from your CLI you can always kill it by hitting `Ctrl + C`.

```
./gitea web
```

## Troubleshooting

Older Linux distributions (such as Debian 7 and CentOS 6) may not be able to load the Gitea binary, usually resulting an error like ```./gitea: /lib/x86_64-linux-gnu/libc.so.6: version `GLIBC_2.14' not found (required by ./gitea)```. This is due to the integrated SQLite support in the binaries we provide. In the future, we will provide binaries without the requirement for glibc. As a workaround, you can upgrade your distribution or [install from source]({{< relref "from-source.en-us.md" >}}).

## Anything missing?

Are we missing anything on this page? Then feel free to reach out to us on our [Gitter channel](https://gitter.im/go-gitea/gitea/), there you will get answers to any question pretty fast.
