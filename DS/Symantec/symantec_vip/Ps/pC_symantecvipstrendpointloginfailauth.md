#### Parser Content
```Java
{
Name = "symantec-vip-str-endpoint-login-fail-auth"
Vendor = "Symantec"
Product = "Symantec VIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [
"""StatusMessage: Authentication Failed"""
]
Fields = [
"""INFO.*?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d \w+(\+|\-)\d+)\s*\"\s+\S+\s+({service_name}[^\":]+)"""
"""for user \[({user}[^\]\s]+)"""
"""({failure_reason}Authentication Failed)"""
]
ParserVersion = "v1.0.0"


}
```