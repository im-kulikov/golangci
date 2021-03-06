# Docker image for golangci-lint

Golang build image with tools for check go programs.

## Contains

* git
* make
* bash
* curl
* dep
* gcc
* musl-dev
* golangci-lint

## Config example

See [example](/.golangci.yml)

```yaml
# https://habr.com/company/roistat/blog/413175/
# https://github.com/golangci/golangci-lint
linters-settings:
  govet:
    check-shadowing: true
  golint:
    min-confidence: 0
  gocyclo:
    min-complexity: 30
  maligned:
    suggest-new: true
  dupl:
    threshold: 100
  goconst:
    min-len: 2
    min-occurrences: 2

linters:
  enable-all: true
```