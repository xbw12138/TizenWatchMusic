# XMusic for Tizen

## Install

```
yarn
```
## Run

### Browser
```
yarn start:web
```

### Windows

```
yarn electron-dev
```

## Build

```
yarn build
```

## Build Tizen wgt


```
tizen build-web -- .
tizen package --type wgt --sign xbw14250 -- ./.buildResult
tizen install -- ./.buildResult -n XMusic.wgt
```

if no certificate

```
tizen certificate -a xbw14250 -p xbw12138 -f mycert14250

tizen security-profiles add -n xbw14250 -a /Users/xubowen/tizen-studio-data/keystore/author/mycert14250.p12 -p xbw12138

tizen cli-config -g default.profiles.path=/Users/xubowen/tizen-studio-data/profile/profiles.xml
```