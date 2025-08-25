# Code Changes for microsoft-o365-cef-app-file-success-displayname (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | os | ['"(os|Platform)":\s*"({os}[^"]+)"', '"Device OS.*?value":"({os}[^"]+)"', '"DeviceOSType".*?newValue":"\[?\\?"({os}[^"\\]+)\\?"\]?', '"Platform":\s*"({os}[^"]+)"', '"value":"({os}[^"]+)","key":"Device OS'] | ['"(os|Platform)":\s*"({os}[^"]+)"', '"Device OS.*?value":"({os}[^"]+)"', '"DeviceOSType"[^\}]+?"newValue":"[\[\\"]*({os}[\w\s]+?)[\\"\]]*\},', '"Platform":\s*"({os}[^"]+)"', '"value":"({os}[^"]+)","key":"Device OS'] |