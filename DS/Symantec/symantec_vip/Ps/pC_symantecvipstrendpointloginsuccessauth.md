#### Parser Content
```Java
{
Name = "symantec-vip-str-endpoint-login-success-auth"
Vendor = "Symantec"
Product = "Symantec VIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [
"""text=Authentication Success for user"""
"""StatusMessage: Success"""
]
Fields = [
"""INFO.*?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d \w+(\+|\-)\d+)\s*\"\s+\S+\s+({service_name}[^\":]+)"""
"""for user \[({user}[^\]\s]+)"""
]
ParserVersion = "v1.0.0"


}
```