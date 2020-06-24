# Clojure development environment setup

## Required dependencies

Install `GraalVM`

Install `clojure`

## Optional dependencies

> Examples assume GraalVM's `bin/` folder has been added to `$PATH`

### Build a standalone executable, uses GraalVM's ahead-of-time (AOT) compilation

Install `GraalVM`'s `native-image` utility. [(documentation)](https://www.graalvm.org/docs/reference-manual/native-image/#install-native-image)

```shell
$ gu install native-image
```

### Deploy build files

Install `maven`

```shell
$ brew install maven
```

### Use Python libraries in Clojure

Install Python

Install Pip(?)

Use dependencies in a `clojure` project's `deps.edn` file

```clojure
{:deps {org.clojure/clojure {:mvn/version "1.10.1"}
        cnuernber/libpython-clj {:mvn/version "1.36"}}}
```

Install Python libraries, in project folder...?

```shell
$ pip3 install seaborn
$ pip3 install matplotlib
```

Use python libraries... TBD

```clojure
(ns example.core
    (:require [libpython-clj.require :refer [require-python]]
    [libpython-clj.python :as py :refer [py. py.. py.-]]))
```
