# xray-configuration

## Scope

This is a configuration for the `XRay` proxy, aiming for speed and simplicity.
The server config is guaranteed to be working on `Ubuntu 24.04.1 LTS` and the client config - on `macOS Tahoe 26.0.1`.

For `iOS` you can use `V2BOX` client.

## Other resources

To install `XRay`, you can use this guide - https://github.com/wpdevelopment11/xray-tutorial (\*)

To see other configuration examples - https://github.com/XTLS/Xray-examples

Official config documentation - https://xtls.github.io/en/config/

## Get values for placeholders

- `USER-ID-1` and `USER-ID-2` - run `xray uuid`.
- `YOUR-PRIVATE-KEY` and `YOUR-PUBLIC-KEY` - run `xray x25519`.
  - `PrivateKey` is your private key.
  - `Password` is your public key.
- `YOUR-VPS-IP` - use the IP of your server.

## How to use

To run `XRay` on your server you can refer to the tutorial I mentioned earlier (\*).

If you run a simple CLI client (for example `brew install xray` for `macOS`), use the provided client config. The proxy will be available on your machine as a simple `SOCKS5` proxy on `localhost:1080`.

## Aliases

You can find useful `.zsh` aliases in `zshrc.txt`.
Note that it's assumed that you put your client config in `~/xray-config.json`.

### SSH-proxy

There are also some aliases for establishing a proxy tunnel through `ssh`. It's a simpler way with no additional configuration needed on the server (except you need to be able to `ssh` into your server without a password), but the download speed is very low.

There's one more placeholder if you want to use this method as well:

- `YOUR-VPS-USER` - a user on your server you can `ssh` to without a password.
