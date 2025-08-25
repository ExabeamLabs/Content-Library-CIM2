# Code Changes for ruckus-r-str-endpoint-login-success-roamsout (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Vendor": "Ruckus", "Product": "Ruckus", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Fields": ["User\s*\[({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w.\-]+))?(@({src_mac}(\w{2}:){5}\w{2}))?\]", "User\s*\[({src_mac}(\w{2}:){5}\w{2})\]", "User\s*\[host\/({src_host}[\w\-]+)(@({src_mac}(\w{2}:){5}\w{2}))?\]", "WLAN\[({ssid}[^\]]+)", "AP\[({wifiap}[^@\]]+)"], "DupFields": ["host->auth_server", "ssid->network", "wifiap->dest_host"], "Name": "ruckus-r-str-endpoint-login-success-roamsout", "Conditions": [" roams out to ", " WLAN[", " AP[", "User["], "ParserVersion": "v1.0.0"} | N/A |