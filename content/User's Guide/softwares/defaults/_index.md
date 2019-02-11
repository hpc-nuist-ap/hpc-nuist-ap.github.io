---
title: "Defaults"
weight: 10
---

You can check the default ENVs by typing `env` in the terminal. It's Dazzled if all are printed ...

Here's the trick to check what you want:

```
$ echo $PATH
# Some important ones:
#	$LIBRARY_PATH, $PATH, $JASPERINC, LD_LIBRARY_PATH
```

{{%expand "**Click to see the result:**" %}}

```
/public/software/mathlib/ncl/bin:/public/software/mpi/openmpi/1.6.5/intel/bin:/opt/gridview//pbs/dispatcher-sched/bin:/opt/gridview//pbs/dispatcher-sched/sbin:/opt/gridview//pbs/dispatcher/bin/lsf_cmd:/opt/gridview//pbs/dispatcher/bin:/opt/gridview//pbs/dispatcher/sbin:/public/software/compiler/composer_xe_2013_sp1.0.080/bin/intel64:/opt/gridview/clusquota//bin:/opt/gridview/clusquota//sbin:/opt/gridview//clusconf/bin:/public/software/ImageMagick/bin:/public/home/test/bin:/usr/local/bin:/usr/bin:/bin:/usr/bin/X11:/usr/X11R6/bin:/usr/games:/opt/kde3/bin:/opt/ibutils/bin:/usr/java/jdk1.6.0_27//bin:/usr/lib/mit/bin:/usr/lib/mit/sbin:/public/software/compiler/pgi/linux86-64/10.6/bin:/public/software/mathlib/cdo/bin:/public/software/mathlib/netcdf/4.3.0/intel/bin:/public/software/mathlib/ncview-2.1.5/bin:/public/software/ncl-6.4.0/bin/:/public/software/mathlib/nco/4.3.7/bin:/public/software/grads/2.0.2/bin
```

{{% /expand%}}

To display the result line by line:

```
$ sed 's/:/\n/g' <<< "$PATH"
```

{{%expand "**Click to see the result:**" %}}

```
/public/software/mathlib/ncl/bin
/public/software/mpi/openmpi/1.6.5/intel/bin
/opt/gridview//pbs/dispatcher-sched/bin
/opt/gridview//pbs/dispatcher-sched/sbin
/opt/gridview//pbs/dispatcher/bin/lsf_cmd
/opt/gridview//pbs/dispatcher/bin
/opt/gridview//pbs/dispatcher/sbin
/public/software/compiler/composer_xe_2013_sp1.0.080/bin/intel64
/opt/gridview/clusquota//bin
/opt/gridview/clusquota//sbin
/opt/gridview//clusconf/bin
/public/software/ImageMagick/bin
/public/home/test/bin
/usr/local/bin
/usr/bin
/bin
/usr/bin/X11
/usr/X11R6/bin
/usr/games
/opt/kde3/bin
/opt/ibutils/bin
/usr/java/jdk1.6.0_27//bin
/usr/lib/mit/bin
/usr/lib/mit/sbin
/public/software/compiler/pgi/linux86-64/10.6/bin
/public/software/mathlib/cdo/bin
/public/software/mathlib/netcdf/4.3.0/intel/bin
/public/software/mathlib/ncview-2.1.5/bin
/public/software/ncl-6.4.0/bin/
/public/software/mathlib/nco/4.3.7/bin
/public/software/grads/2.0.2/bin
```

{{% /expand%}}