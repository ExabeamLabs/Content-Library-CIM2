# Code Changes for pan-gp-cef-vpn-logout-success-globalprotect (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "pan-gp-cef-vpn-logout-success-globalprotect", "Vendor": "Palo Alto Networks", "Product": "GlobalProtect", "TimeFormat": ["epoch", "MMM dd yyyy HH:mm:ss"], "Conditions": ["CEF:", "|Palo Alto Networks|", "|globalprotect", "GlobalProtect gateway user logout succeeded"], "Fields": ["rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)", "\Wrt=({time}\d{13})", "User name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\.?(\s|,|\\"|$)", "User name:\s*({email_address}[^@\s]+@[^\s,]+),", "\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"], "ParserVersion": "v1.0.0"} | N/A |