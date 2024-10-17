#### Parser Content
```Java
{
Name = "symantec-vip-str-endpoint-login-fail-accessreject"
Vendor = "Symantec"
Product = "Symantec VIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [
"""text=Sending Acces-Reject for user"""
]
Fields = [
"""INFO.*?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d \w+)(\+|\-)\d+\s*\"\s+\S+\s+({service_name}[^\":]+)"""
"""for user \[({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""reason=[^;]*;\s*({failure_reason}[^\"]*)"""
]
ParserVersion = "v1.0.0"


}
```