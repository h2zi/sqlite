# GORM SQLite Driver

[![CI](https://github.com/go-gorm/sqlite/workflows/CI/badge.svg)](https://github.com/go-gorm/sqlite/actions)

The official SQLite driver for [GORM](https://gorm.io), based on [go-sqlite3](https://github.com/mattn/go-sqlite3) (requires CGO).

## Quick Start

```go
import (
  "gorm.io/driver/sqlite"
  "gorm.io/gorm"
)

db, err := gorm.Open(sqlite.Open("gorm.db"), &gorm.Config{})
```

> For full documentation, visit [https://gorm.io](https://gorm.io).

## Pure Go Alternatives

If you need a CGO-free SQLite driver, the following community projects are available:

| Driver | Repository |
|--------|------------|
| glebarez/sqlite | [github.com/glebarez/sqlite](https://github.com/glebarez/sqlite) |
| libtnb/sqlite | [github.com/libtnb/sqlite](https://github.com/libtnb/sqlite) |

Usage is identical — simply swap the import path:

```go
import (
  "github.com/glebarez/sqlite" // or "github.com/libtnb/sqlite"
  "gorm.io/gorm"
)

db, err := gorm.Open(sqlite.Open("gorm.db"), &gorm.Config{})
```
