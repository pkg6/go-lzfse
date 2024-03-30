# go-lzfse

[![GoDoc](https://godoc.org/github.com/blacktop/go-lzfse?status.svg)](https://godoc.org/github.com/blacktop/go-lzfse) [![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org)

> Go bindings for [lzfse](https://github.com/lzfse/lzfse) compression.

---

## Install

```bash
go get github.com/pkg6/go-lzfse
```

## Examples

```golang
import (
    "io/ioutil"
    "log"

    lzfse "github.com/pkg6/go-lzfse"
    "github.com/pkg/errors"
)

func main() {

    dat, err := ioutil.ReadFile("encoded.file")
    if err != nil {
        log.Fatal(errors.Wrap(err, "failed to read compressed file"))
    }

    decompressed = lzfse.DecodeBuffer(dat)

    err = ioutil.WriteFile("decoded.file", decompressed, 0644)
    if err != nil {
        log.Fatal(errors.Wrap(err, "failed to decompress file"))
    }
}
```

## Credit

- <https://github.com/zchee/go-lzfse>
- https://github.com/iineva/go-lzfse

## License

MIT Copyright (c) 2019 blacktop
