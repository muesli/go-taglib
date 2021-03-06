go-taglib
=========

Interface to the taglib audio tagging library with MIT license.

## Install

    go get github.com/vbatts/go-taglib/taglib


## Example

    package main

    import "github.com/vbatts/go-taglib/taglib"
    import "fmt"

    func main() {
        f := taglib.Open("foo.mp3")
        if f==nil { return }
        defer f.Close()
        fmt.Printf("%#v\n",f.GetTags())
        fmt.Printf("%#v\n",f.GetProperties())
    }

## Dependencies

On debian:

    apt-get install libtagc0-dev

On Fedora:

    yum install install taglib-devel

On OS X:

    brew install taglib
