# XMRig AMD

:warning: **[Monero changed PoW algorithm on October 18](https://github.com/xmrig/xmrig/issues/753), all miners and proxy should be updated to [v2.8+](https://github.com/xmrig/xmrig-amd/releases/tag/v2.8.5)** :warning:
:warning: **This fork of xmrig-amd miner has known stability issues on some AMD hardware, so use it with caution** :warning:

[![Github All Releases](https://img.shields.io/github/downloads/xmrig/xmrig-amd/total.svg)](https://github.com/MoneroOcean/xmrig-amd/releases)
[![GitHub release](https://img.shields.io/github/release/xmrig/xmrig-amd/all.svg)](https://github.com/MoneroOcean/xmrig-amd/releases)
[![GitHub Release Date](https://img.shields.io/github/release-date-pre/xmrig/xmrig-amd.svg)](https://github.com/MoneroOcean/xmrig-amd/releases)
[![GitHub license](https://img.shields.io/github/license/xmrig/xmrig-amd.svg)](https://github.com/MoneroOcean/xmrig-amd/blob/master/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/xmrig/xmrig-amd.svg)](https://github.com/MoneroOcean/xmrig-amd/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/xmrig/xmrig-amd.svg)](https://github.com/MoneroOcean/xmrig-amd/network)

XMRig is high performance Monero (XMR) OpenCL miner, with the official full Windows support.

GPU mining part based on [Wolf9466](https://github.com/OhGodAPet) and [psychocrypt](https://github.com/psychocrypt) code.

* This is the AMD (OpenCL) GPU mining version, there is also a [CPU version](https://github.com/MoneroOcean/xmrig) and [NVIDIA GPU version](https://github.com/MoneroOcean/xmrig-nvidia).
* [Roadmap](https://github.com/MoneroOcean/xmrig/issues/106) for next releases.

:warning: Suggested values for GPU auto configuration can be not optimal or not working, you may need tweak your threads options. Please fell free open an [issue](https://github.com/MoneroOcean/xmrig-amd/issues) if auto configuration suggest wrong values.

<img src="https://i.imgur.com/TFncsi7.png" width="696" >

#### Table of contents
* [Features](#features)
* [Download](#download)
* [Usage](#usage)
* [Build](https://github.com/MoneroOcean/xmrig-amd/wiki/Build)
* [Donations](#donations)
* [Release checksums](#release-checksums)
* [Contacts](#contacts)

## Features
* High performance.
* Official Windows support.
* Support for backup (failover) mining server.
* CryptoNight-Lite support for AEON.
* Automatic GPU configuration.
* Nicehash support.
* It's open source software.

## Download
* Binary releases: https://github.com/MoneroOcean/xmrig-amd/releases
* Git tree: https://github.com/MoneroOcean/xmrig-amd.git
  * Clone with `git clone https://github.com/MoneroOcean/xmrig-amd.git`  :hammer: [Build instructions](https://github.com/MoneroOcean/xmrig-amd/wiki/Build).

## Usage
Use [config.xmrig.com](https://config.xmrig.com/amd) to generate, edit or share configurations.

### Command line options
```
-a, --algo=ALGO              specify the algorithm to use
                                 cryptonight
                                 cryptonight-lite
                                 cryptonight-heavy
  -o, --url=URL                URL of mining server
  -O, --userpass=U:P           username:password pair for mining server
  -u, --user=USERNAME          username for mining server
  -p, --pass=PASSWORD          password for mining server
      --rig-id=ID              rig identifier for pool-side statistics (needs pool support)
  -k, --keepalive              send keepalived for prevent timeout (needs pool support)
      --nicehash               enable nicehash.com support
      --tls                    enable SSL/TLS support (needs pool support)
      --tls-fingerprint=F      pool TLS certificate fingerprint, if set enable strict certificate pinning
  -r, --retries=N              number of times to retry before switch to backup server (default: 5)
  -R, --retry-pause=N          time to pause between retries (default: 5)
      --opencl-devices=N       list of OpenCL devices to use.
      --opencl-launch=IxW      list of launch config, intensity and worksize
      --opencl-strided-index=N list of strided_index option values for each thread
      --opencl-mem-chunk=N     list of mem_chunk option values for each thread
      --opencl-comp-mode=N     list of comp_mode option values for each thread
      --opencl-affinity=N      list of affinity GPU threads to a CPU
      --opencl-platform=N      OpenCL platform index
      --opencl-loader=N        path to OpenCL-ICD-Loader (OpenCL.dll or libOpenCL.so)
      --print-platforms        print available OpenCL platforms and exit
      --no-cache               disable OpenCL cache
      --no-color               disable colored output
      --variant                algorithm PoW variant
      --donate-level=N         donate level, default 5% (5 minutes in 100 minutes)
      --user-agent             set custom user-agent string for pool
  -B, --background             run the miner in the background
  -c, --config=FILE            load a JSON-format configuration file
  -l, --log-file=FILE          log all output to a file
  -S, --syslog                 use system log for output messages
      --print-time=N           print hashrate report every N seconds
      --api-port=N             port for the miner API
      --api-access-token=T     access token for API
      --api-worker-id=ID       custom worker-id for API
      --api-id=ID              custom instance ID for API
      --api-ipv6               enable IPv6 support for API
      --api-no-restricted      enable full remote access (only if API token set)
      --dry-run                test configuration and exit
  -h, --help                   display this help and exit
  -V, --version                output version information and exit
```

## Donations
Default donation 5% (5 minutes in 100 minutes) can be reduced to 1% via option `donate-level`.

* XMR: `48edfHu7V9Z84YzzMa6fUueoELZ9ZRXq9VetWzYGzKt52XU5xvqgzYnDK9URnRoJMk1j8nLwEVsaSWJ4fhdUyZijBGUicoD`
* BTC: `1P7ujsXeX7GxQwHNnJsRMgAdNkFZmNVqJT`

## Release checksums
### SHA-256
```
6db86c76d245a5ab1f49c15ac7284d287349340032fb231ead7bd1064239dc66 xmrig-amd-2.8.5-xenial-amd64.tar.gz/xmrig-amd-2.8.5/xmrig-amd
ab2e419467dd332ec2832a7bda1ffe15a50eb1c1d1ecd442d249284554fc2c54 xmrig-amd-2.8.5-xenial-amd64.tar.gz/xmrig-amd-2.8.5/xmrig-amd-notls
af55fb2d4de756a7c7fe2d702807a7f9cf991c7463f347d13cc31dbb2d5a38c0 xmrig-amd-2.8.5-win64.zip/xmrig-amd.exe
d09c35a06b00500ab07ad1b06da06e7cd0435964f76e777498bef79bc51a5719 xmrig-amd-2.8.5-win64.zip/xmrig-amd-notls.exe
```

## Contacts
* support@xmrig.com
* [reddit](https://www.reddit.com/user/XMRig/)
* [twitter](https://twitter.com/xmrig_dev)
