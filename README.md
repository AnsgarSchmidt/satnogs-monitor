# SatNOGS Monitor (WIP)

![Screenshot](/doc/screen.png)

## WIP

This is more of a proof of concept for now. I'm playing with different
architectures and layouts, so expect everything to change rapidly. Feel free to
open issues or find me on the [SatNOGS irc
channel](https://satnogs.org/contact/) if you have suggestions what info about
your station is useful to you and should be included. There is also a
corresponding forum post at the [SatNOGS community
forum](https://community.libre.space/t/satnogs-station-monitor/2802)

## TODOs / planned features

Note: the list is by no means complete or in any particular order.

- [ ] visual alerts on station failure (failed obs, no heartbeats, ...)
- [ ] rotator state
- [ ] support multiple stations
- [ ] theme support
- [ ] network overview
- [ ] GUI
- [ ] cross platform
- [ ] waterfall stream of current observation
- [ ] audio stream of current observation

## Dependencies

### libgpredict

See [libgpredict](https://github.com/cubehub/libgpredict) for details.

```
git clone https://github.com/cubehub/libgpredict.git
cd libgpredict
mkdir build
cd build
cmake ../
make
make install
sudo ldconfig # for linux
```

### Rust

Use your distribution package management to install ```rustup``` if possible.
See [Install Rust](https://www.rust-lang.org/en-US/install.html).

You'll need the *beta* or *nightly* version until Editions are in *stable*.

```
rustup install beta
```
or
```
rustup install nightly
```

### A true color terminal

While other terminals will be supported in the future, the screenshot was taken
using [alacritty](https://github.com/jwilm/alacritty) with the [Lucy
Tewi](https://github.com/lucy/tewi-font) font.

## Hacking

```
git clone https://github.com/wose/satnogs-monitor.git
cd satnogs-monitor/monitor
mkdir ~/.config/satnogs-monitor
cp examples/config.toml ~/.config/satnogs-monitor/
edit ~/.config/satnogs-monitor
cargo +beta run --release
```
