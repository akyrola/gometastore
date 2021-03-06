## hmstool table list

list tables

### Synopsis

List tables matching specified pattern. By default list all table names.

The pattern can be specified in two ways and it affects the way it is applied.
It can be just added on the command line in which case all table names are fetched from HMS
and glob style matching is applied. Alternatively, if the pattern is specified with -M flag,
the glob pattern is passed to the server. This can be useful when there are a lot of tables.

Examples:

    hmstool table list -d default "*customer"
    hmstool table list -d default -M "*customer"

Both of these commands will show all table names in the default database 
which have customer in their name, but the first one will use client-side
matching and the second one will use server-side matching.


```
hmstool table list [flags]
```

### Options

```
  -h, --help           help for list
  -l, --long           show table info
  -M, --match string   only return tables matching pattern
```

### Options inherited from parent commands

```
      --config string   config file (default is $HOME/.hmstool.yaml)
  -d, --dbname string   database name
  -H, --host string     hostname for HMS server (default "localhost")
  -o, --output string   output file
  -U, --owner string    owner name (default "hive")
  -p, --port string     port for HMS server (default "9083")
  -t, --table string    table name
      --ts int          timestamp
```

### SEE ALSO

* [hmstool table](hmstool_table.md)	 - table operations

###### Auto generated by spf13/cobra on 9-Oct-2018
