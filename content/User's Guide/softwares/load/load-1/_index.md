---
title: "Matlab"
weight: 10
---

Matlab isn't loaded by default:

```
$ which matlab
```

{{%expand "**Click to see the result:**" %}}

```
which: no matlab in (/public/software/mathlib/ncl/bin:/public/software/mpi/openmpi/1.6.5/intel/bin:/opt/gridview//pbs/dispatcher-sched/bin:/opt/gridview//pbs/dispatcher-sched/sbin:/opt/gridview//pbs/dispatcher/bin/lsf_cmd:/opt/gridview//pbs/dispatcher/bin:/opt/gridview//pbs/dispatcher/sbin:/public/software/compiler/composer_xe_2013_sp1.0.080/bin/intel64:/opt/gridview/clusquota//bin:/opt/gridview/clusquota//sbin:/opt/gridview//clusconf/bin:/public/software/ImageMagick/bin:/public/home/test/bin:/usr/local/bin:/usr/bin:/bin:/usr/bin/X11:/usr/X11R6/bin:/usr/games:/opt/kde3/bin:/opt/ibutils/bin:/usr/java/jdk1.6.0_27//bin:/usr/lib/mit/bin:/usr/lib/mit/sbin:/public/software/compiler/pgi/linux86-64/10.6/bin:/public/software/mathlib/cdo/bin:/public/software/mathlib/netcdf/4.3.0/intel/bin:/public/software/mathlib/ncview-2.1.5/bin:/public/software/ncl-6.4.0/bin/:/public/software/mathlib/nco/4.3.7/bin:/public/software/grads/2.0.2/bin)
```

{{% /expand%}}

Let's find where is Matlab:

```
$ ls /datadir1/software/MATLAB/

# output:
# 	R2017a  R2018a
```

Choose which one you prefer and add it to `~/.profile` by Vi editor:

```
export PATH=$PATH:/datadir1/software/MATLAB/R2018a/bin
```

Then source your config file in terminal and check again:

```
$ source ~/.profile
$ which matlab

# output:
# 	/datadir1/software/MATLAB/R2018a/bin/matlab
```