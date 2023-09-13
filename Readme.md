# go-sqlite3-extension-functions

## Install

```bash
sudo aptitude install libsqlite3-dev # for ubuntu

mkdir ./build
cd ./build
cmake ..
make && sudo make install
```

## What

This is the same file contributed by Liam Healy on 2010-02-06 15:45:07 at [https://www.sqlite.org/contrib?orderby=date](https://www.sqlite.org/contrib?orderby=date)

All this does is use `CMake` to create a cross-platform build that can be used in [go-sqlite3](https://github.com/mattn/go-sqlite3)

## Usage

Use like so:

```go
package main

import (
	"database/sql"

	sqlite3 "github.com/mattn/go-sqlite3"
	"github.com/dinedal/go-sqlite3-extension-functions/go"
)

func Main() {
	db, err := sql.Open("sqlite3-extension-functions", ":memory:")
}
```

Or use the code in [extension-functions.go](/go/extension-functions.go) to create your own driver hook.

## Full function list

Math: acos, asin, atan, atn2, atan2, acosh, asinh, atanh, difference, degrees, radians, cos, sin, tan, cot, cosh, sinh, tanh, coth, exp, log, log10, power, sign, sqrt, square, ceil, floor, pi. String: replicate, charindex, leftstr, rightstr, ltrim, rtrim, trim, replace, reverse, proper, padl, padr, padc, strfilter. Aggregate: stdev, variance, mode, median, lower_quartile, upper_quartile
