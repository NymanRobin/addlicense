# addlicense

The program ensures source code files have copyright license headers
by scanning directory patterns recursively.

It modifies all source files in place and avoids adding a license header
to any file that already has one.

## install

    go get -u github.com/google/addlicense

## usage

    addlicense [flags] pattern [pattern ...]

    -c copyright holder (defaults to "Google LLC")
    -f custom license file (no default)
    -l license type: apache, bsd, mit, mpl (defaults to "apache")
    -y year (defaults to current year)
    -check check only mode: verify presence of license headers and exit with non-zero code if missing
    -config yaml config file: see examples/config.yml

The pattern argument can be provided multiple times, and may also refer
to single files.

## configuration
Paths to be ignored by addlicense can be configured in a yaml config file and passed to addlicense using the `-config` option. Patterns that determine whether a file already has a license and file extension comment commenting formats can also be configured there. For an example, see the example [config.yml](https://github.com/nokia/addlicense/blob/master/examples/config.yml).

## license

Apache 2.0

This is not an official Google product.
