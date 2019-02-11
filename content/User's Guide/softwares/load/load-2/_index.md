---
title: "Python"
weight: 15
---

Python's version is 2.6.8 by default. For scientific purpose, it's lack of many packages and out-of-date version.

We've created our **own Anaconda mirror and two environments (python2.7 and python3.6)**.

There're two options for you: use installed environment and create your own python environment.

### Use installed one

- **Python2.7**

  add these lines to`~/.profile`:

  ```
  export PATH=/public/software/anaconda/anaconda3/bin:$PATH
  . /public/software/anaconda/anaconda3/etc/profile.d/conda.sh
  conda activate python27
  ```

- **Python3.6**

  add these lines to`~/.profile`:

  ```
  export PATH=/public/software/anaconda/anaconda3/bin:$PATH
  . /public/software/anaconda/anaconda3/etc/profile.d/conda.sh
  conda activate python36
  ```

- **Check installed packages**

  ```
  $ conda list
  # If you need more packages, plead add to the end of `/public/software/anaconda/requirements.txt`.
  ```

### Create own one

The mirror of Anaconda is located at these directory:

```
/public/software/anaconda/archive
/public/software/anaconda/pkgs
```

You can just run `/public/software/anaconda/archive/<Anaconda****.sh>` to install at your own directory.

### Set mirror

If you choose to install your own anaconda, you should set mirror to speed up installing packages. Choose preferred method below and edit `~/.condarc  `as same as example:

- Local mirror (fastest, updated once a month)

  ```
  allow_other_channels : false
  channel_alias: file://public/software/anaconda/pkgs
  channels:
    - free
    - main
    - pro
    - conda-forge
  offline: true
  ```

- Tsinghua mirror (slow, lastest)

  ```
  channels:
    - defaults
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
  show_channel_urls: true
  ```