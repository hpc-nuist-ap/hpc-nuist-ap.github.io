---
title: "Python"
weight: 15
---

Python's version is 2.6.8 by default. For scientific purpose, it's lack of many packages and out-of-date version.

~~We've created our **own Anaconda mirror and two environments (python2.7 and python3.6)**.~~

Since the tsinghua mirror has been [removed](https://mirror.tuna.tsinghua.edu.cn/news/close-anaconda-service/) once, we set up the Python environment based on official sources now.

There're two options for you to use Python:

1. Use installed environment;
2. Create your own Python environment.

### Use installed one

- **Python3.7**

  add these lines to `~/.profile`:

  ```
  export PATH=/public/software/anaconda/anaconda3/bin:$PATH
  . /public/software/anaconda/anaconda3/etc/profile.d/conda.sh
  conda activate python37
  ```

- **Check installed packages**

  ```
  $ conda list
  # If you need more packages, plead add to the end of `/public/software/anaconda/requirements.txt`.
  ```

- **Add more packages**

  If you can't find specific package, you can edit `/public/software/anaconda/requirements.txt` according to the instruction at the end of that file.

  After the package is installed, you'll get an email.

### Create your own

1. Download the newest installer file from [anaconda_archive](https://repo.anaconda.com/archive/) or [miniconda_archive](https://repo.anaconda.com/miniconda/). It's better to install miniconda and create an [virtual environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).
2. Run the downloaded installer file to install anaconda to any new directory under your account.
3. Add the PATH to the environment variable.
4. Edit `~/.condarc  ` to add more channels:

```
channels:
  - free
  - main
  - pro
  - conda-forge
show_channel_urls: True
allow_other_channels: True
```