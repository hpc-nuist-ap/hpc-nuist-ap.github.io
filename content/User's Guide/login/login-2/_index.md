---
title: "CLI"
description: "Command line interface (Win/Mac/Linux/Unix)"
weight: 15
---

- Open terminal

  - Win: Recommend [MobaXterm](https://mobaxterm.mobatek.net/) or [Git](https://git-scm.com/downloads)
  - Mac/Linux/Unix: Terminal

- Type in the terminal

  ```
  $ ssh <username>@<IP_address>
  ```

  Now you probably want to avoid taping this long command to connect to the platform. You can customize SSH aliases for that.

  Edit the file `~/.ssh/config` (create it if it does not already exist) and adding the following entries:

  ```
  Host ap-cluster
      Hostname <IP_address>
      User <username>
      ServerAliveInterval 60
  ```

  Now you shall be able to issue the following (simpler) command to connect to the cluster and obtain the welcome banner:

  ```
  $ ssh ap-cluster
  ```

  