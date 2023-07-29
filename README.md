# Building xmrig with Embedded Config

```
apt-get install git build-essential cmake libuv1-dev libssl-dev libhwloc-dev
```
```
git clone -b dev https://github.com/xmrig/xmrig.git
```
edit `/src/core/config/Config_default.h` and put your wallet and Mining pool

go to `/src/donate.h` and change `constexpr const int kDefaultDonateLevel = 1;`
`constexpr const int kMinimumDonateLevel = 1;` to 0

```
mkdir xmrig/build && cd xmrig/build
```
```
cmake .. -DWITH_EMBEDDED_CONFIG=ON
```
```
make -j$(nproc)
```
