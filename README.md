# Wi-Fi QR Code Printout

A [single HTML page](https://staticbr.github.io/wifi-qr-printout/) that turns a Wi-Fi network name and password into a printable QR code sign. Guests scan it with their phone camera and connect automatically.

## Usage

1. Open [https://staticbr.github.io/wifi-qr-printout/](https://staticbr.github.io/wifi-qr-printout/) in any browser.
2. Enter the network name, password and security type.
3. Adjust the headline, subtitle and footer text if you like.
4. Click **Print**.

## URL parameters

All fields can be prefilled via the URL, e.g. to bookmark or share a ready-made sign:

```
https://staticbr.github.io/wifi-qr-printout/?ssid=MyHomeWiFi&password=secret123&title=Welcome!&footer=Enjoy%20your%20stay
```

| Parameter      | Values                       | Default            |
| -------------- | ---------------------------- | ------------------ |
| `ssid`         | network name                 | –                  |
| `password`     | network password             | –                  |
| `security`     | `WPA`, `WEP`, `nopass`       | `WPA`              |
| `hidden`       | `1` / `0`                    | `0`                |
| `title`        | headline text                | `Connect to Wi-Fi` |
| `subtitle`     | subtitle text                | `Scan to connect`  |
| `footer`       | footer note                  | –                  |
| `showssid`     | `1` / `0`                    | `1`                |
| `showpassword` | `1` / `0`                    | `1`                |
| `showicon`     | `1` / `0`                    | `1`                |
| `print`        | `1` / `0` – show only the sign, no settings | `0` |

Yes/no options also accept `true`/`false`, `yes`/`no` and `on`/`off`. Parameter names and `security` values are case-insensitive. URL-encode special characters (space → `%20`, `&` → `%26`, `#` → `%23`).

Note: a password in a URL ends up in browser history and, if hosted, in server logs.

## Features

- Supports WPA/WPA2/WPA3, WEP, open and hidden networks
- Print-ready A4 layout
- Customizable text, with options to show or hide the network name, password and icon
- Readable font for passwords that keeps `0`/`O` and `1`/`l`/`I` distinct
- Fully self-contained: no external requests, works offline, nothing is stored or uploaded

## Credits

- [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) by Kazuhiko Arase – MIT License
- [Atkinson Hyperlegible Mono](https://www.brailleinstitute.org/freefont/) by Braille Institute – SIL Open Font License 1.1
