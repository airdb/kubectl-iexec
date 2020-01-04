# Kubectl Interactive Exec

## Summary

`Kubectl-iexec` is a plugin providing an interactive selector to exec into a running pod. For a search filter, the plugin will return a list of pods and containers that match, then perform a `kubectl exec` to the selection.

_Notes:_

[reference](https://github.com/gabeduke/kubectl-iexec/)

Kubectl >= `v1.12.0` is required for plugins to work

For more information on kuberctl plugins see [documentation](https://kubernetes.io/docs/tasks/extend-kubectl/kubectl-plugins/)


## Usage:

```
$ kubectl iexec --help

Kubectl-iexec is an interactive pod and container selector for `kubectl exec`

Arg[1] will act as a filter, any pods that match will be returned in a list
that the user can select from. Subsequent args make up the array of commands that
should be executed on the pod.

example:
kubectl iexec busybox /bin/sh

example:
kubectl iexec busybox cat /etc/hosts

Usage:
  iexec [pod filter] [remote command(s)] [flags]

Flags:
  -c, --container string   Container to search
  -h, --help               help for iexec
  -l, --log-level string   log level (trace|debug|info|warn|error|fatal|panic)
  -x, --naked              Decolorize output
  -n, --namespace string   Namespace to search
  -v, --vim-mode            Vim Mode enabled
```


## Install:

To install the plugin, the binary simply needs to be somewhere on your path in the format kubectl-[plugin_name]. 

```
https://github.com/airdb/adb/releases/latest/download/adb
https://github.com/airdb/adb/releases/latest/download/adb-darwin
```

