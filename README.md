# setup-typedb

GitHub Action for installing and running TypeDB

## Arguments

| Argument           | Description                            | Default | Value                                                                                         |
|--------------------|----------------------------------------|---------|-----------------------------------------------------------------------------------------------|
| `typedb_version`   | The version of TypeDB to use           | latest  | A TypeDB version (e.g. `3.5.0`) or `latest`                                                   |
| `typedb_grpc_port` | TypeDB's port for gRPC connections     | 1729    | Valid port number                                                                             |
| `typedb_http_port` | TypeDB's port for HTTP connections     | 8000    | Valid port number                                                                             |
| `typedb_args`      | Additional arguments to pass to TypeDB |         | TypeDB CLI arguments - see https://typedb.com/docs/maintenance-operation/typedb-configuration |

## Example

```yaml
name: TypeDB CI

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - name: Git checkout
      uses: actions/checkout@v2
    - name: Run TypeDB
      uses: typedb/setup-typedb@v1
      with:
        typedb_version: 3.5.1
```

## Licensing

Released under the Mozilla Public License 2.0 (MPL 2.0).
For license information, please see [LICENSE](https://github.com/typedb/setup-typedb/blob/master/LICENSE). 
