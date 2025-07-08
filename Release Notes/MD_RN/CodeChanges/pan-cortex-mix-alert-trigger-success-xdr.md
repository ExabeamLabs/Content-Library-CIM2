# Code Changes for pan-cortex-mix-alert-trigger-success-xdr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain | ["\Wsuser=\['(((NT AUTHORITY|TEST|({domain}[^\\\=]+))\\+)?(({user}N\/A|LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?)))(',\s|'\]\s+\w+=)"] | ["\Wsuser=\['(((NT AUTHORITY|TEST|({domain}[^\\\=]+))\\+)?(N\/A|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?)))(',\s|'\]\s+\w+=)"] |
| edit_regex_field | time | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)', '({time}\w+\s+\d+\s\d\d:\d\d:\d\d)\s\w+'] |
| edit_regex_field | user | ["\Wsuser=\['(((NT AUTHORITY|TEST|({domain}[^\\\=]+))\\+)?(({user}N\/A|LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?)))(',\s|'\]\s+\w+=)"] | ["\Wsuser=\['(((NT AUTHORITY|TEST|({domain}[^\\\=]+))\\+)?(N\/A|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?)))(',\s|'\]\s+\w+=)"] |