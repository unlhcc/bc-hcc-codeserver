# Batch Connect - HCC Code Server

[![pipeline status](https://git.unl.edu/hcc/bc-hcc-codeserver/badges/master/pipeline.svg)](https://git.unl.edu/hcc/bc-hcc-codeserver/-/commits/master)
[![GitHub License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

An improved file viewer / editor for OSC OnDemand that launches a
Code Server within an Owens batch job. Code Server leverages VSCode as its
editor.

## Prerequisites

This Batch Connect app requires the following software be installed on the
**compute nodes** that the batch job is intended to run on (**NOT** the
OnDemand node):

- [Lmod] 6.0.1+ or any other `module purge` and `module load <modules>` based
  CLI used to load appropriate environments within the batch job before
  launching Code server.
- [Code Server] 2.x+ available from Github: https://github.com/cdr/code-server/releases

[Code Server]: https://coder.com/
[Lmod]: https://www.tacc.utexas.edu/research-development/tacc-projects/lmod
[VS Code]: https://code.visualstudio.com/

## Build/Install

Gitlab CI will automatically build both CentOS 7 and 8 RPMs.
They can be installed directly via `yum` for testing.
For production, add to the per-cluster common repos and require via puppet.

## Known Issues

- In-app installation of extensions does not work
- The authentication provided by code-server is unencrypted

## Contributing

1. Fork it ( https://git.unl.edu/hcc/bc-hcc-matlab )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
