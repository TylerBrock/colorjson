Color JSON Pretty Printer for Go
================================

This package is based heavily on hokaccha/go-prettyjson but has some noticible differences:
 - faster (recursive descent serializer)
 - more customizable (ability to have zero indent, print raw json strings, etc...)
 - better defaults (less bold colors)

Installation
------------

```sh
go get -u github.com/TylerBrock/colorjson
```

Usage
-----

```go
import "github.com/TylerBrock/colorjson"

v := map[string]interface{}{
    "str": "foo",
    "num": 100,
    "bool": false,
    "null": nil,
    "array": []string{"foo", "bar", "baz"},
    "map": map[string]interface{}{
        "foo": "bar",
    },
}

s, _ := colorjson.Marshal(v)
fmt.Println(string(s))
```
