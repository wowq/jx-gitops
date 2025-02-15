## jx-gitops gc jobs

garbage collection for jobs

***Aliases**: job*

### Usage

```
jx-gitops gc jobs
```

### Synopsis

Garbage collect old Jobs that have completed or failed

### Examples

  # garbage collect old jobs of the default age keeping 1
  jx gitops gc jobs
  
  # garbage collect jobs older than 10 minutes and keeping 10
  jx gitops gc jobs -a 10m -k 10
  
  # garbage collect jobs older than 10 (don't keep any job)
  jx gitops gc jobs -a 10m -k 0
  
  # dry run mode
  jx gitops gc jobs --dry-run

### Options

```
  -a, --age duration       The minimum age of jobs to garbage collect. Any newer jobs will be kept (default 1h0m0s)
  -d, --dry-run            Dry run mode. If enabled just list the jobs that would be removed
  -h, --help               help for jobs
  -k, --keep int           The minimum jobs to keep. Jobs to keep even if they are older than the age parameter (default 1)
  -n, --namespace string   The namespace to look for the jobs. Defaults to the current namespace
  -s, --selector string    The selector to use to filter the jobs
```

### SEE ALSO

* [jx-gitops gc](jx-gitops_gc.md)	 - Commands for garbage collecting resources

###### Auto generated by spf13/cobra on 14-Jan-2022
