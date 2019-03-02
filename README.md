# openwrt-packages-mackerel-plugin-smartmeter [![Build Status](https://secure.travis-ci.org/hnw/openwrt-packages-mackerel-plugin-smartmeter.svg?branch=master)](https://travis-ci.org/hnw/openwrt-packages-mackerel-plugin-smartmeter)

This is [mackerel-plugin-smartmeter](https://github.com/hnw/mackerel-plugin-smartmeter/) package for OpenWrt, tested on OpenWrt 15.05.1 / LEDE 17.01.4.

# How to install binary package

See also [hnw/openwrt-packages](https://github.com/hnw/openwrt-packages).

```
# opkg install kmod-usb-acm
# opkg install mackerel-agent
# uci set mackerel-agent.@mackerel-agent[0].apikey=[APIKEY]
# opkg install mackerel-plugin-smartmeter
```

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot:

```
$ echo 'src-git hnw_mackerel-plugin-smartmeter https://github.com/hnw/openwrt-packages-mackerel-plugin-smartmeter.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install mackerel-plugin-smartmeter
$ make packages/mackerel-plugin-smartmeter/compile
```
