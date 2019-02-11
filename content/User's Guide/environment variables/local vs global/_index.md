---
title: "Local vs Global"
weight: 10
---

### Global ENV

If an ENV is defined as a global scope variable, its value is defined for **all the programs or scripts run in that terminal**.

Define a global env in terminal:

```
$ export <varname>=<value>
```

{{% notice note %}}
There is no space between name, =, and value. Otherwise,  each of the three will be considered as a separate command, thus raising an error.
{{% /notice %}}

Now, Just place a `$` before the `varname` and Linux will take care of replacing it with its value.

Type on the command line or use it in any script:

```
$ echo $<varname>
```

*echo command is just an example, environment variables can be used in the same way with any Linux command.*

{{% notice note %}}
Global ENVs are global only in the context of a terminal from which it is defined, Hence even being global ENV will not be valid for a terminal other than the genesis terminal of the ENV. <br></br>
For persisting the ENV, This is what we will explore in [Persisting ENVs](https://hpc-nuist-ap.github.io/users-guide/environment-variables/persisting-envs/) section.
{{% /notice %}}

### Local ENV

Local scoped ENVs can **only be accessed by the terminal itself** and not by any program or shell script even if the latter is started by the same terminal for which the local scoped ENV is defined.

Define a local env in terminal:

```
$ <varname>=<value>
```

{{% notice note %}}
Accessing local scoped ENV is done the same way you access a global scoped ENV.
{{% /notice %}}

### Commands

| Command                    | Description                             |
| -------------------------- | --------------------------------------- |
| `echo $<varname>`          | To display value of a variable          |
| `env`                      | Displays all environment variables      |
| `<varname>=<value>`        | Create a new local variable             |
| `unset  <varname>`         | Remove a variable                       |
| `export <varname>=<value>` | To set value of an environment variable |

#### *References*

1. [Linux Environment Variables](https://codeburst.io/linux-environment-variables-53cea0245dc9)
2. [List of Environment Variables in Linux/Unix](https://www.guru99.com/linux-environment-variables.html)