#### Parser Content
```Java
{
Name = "f5-apm-mix-vpn-success-01490"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""01490"""
""":5:"""
"""Username """
]
Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s"""
"""\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
"""hostname="({host}[\w\-.]+)"""
""""host":\{"name":"({host}[^"]+)"""
"""\s01490\d+:5:.*?({session_id}[^\s:]+): (Username|Retry)"""
"""\sUsername\s+'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s*'"""
]
ParserVersion = "v1.0.0"


}
```