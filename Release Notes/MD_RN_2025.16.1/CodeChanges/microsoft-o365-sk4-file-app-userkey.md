# Code Changes for microsoft-o365-sk4-file-app-userkey (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | removable_media_serial_number |  | ['"SerialNumber":\s*"({removable_media_serial_number}[^"]+)"'] |
| edit_regex_field | removable_media_vendor |  | ['"Manufacturer":\s*"({removable_media_vendor}[^"]+)"'] |