#### Parser Content
```Java
{
Name = "f5-apm-mix-vpn-success-01490"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
ExtractionType = json
Conditions = [
"""01490"""
""":5:"""
"""Username """
]
Fields = [
"""({time}\w+ \d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
"""hostname="({host}[\w\-.]+)"""
""""host":\{"name":"({host}[^"]+)"""
"""\s01490\d+:5:.*?({session_id}[^\s:]+): (Username|Retry)"""
"""\sUsername\s+'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*'"""
"""\sAccess_Profile="({access_group}[^"]+)""""
"""exa_regex=({time}\w+ \d+ \d+:\d+:\d+)"""
"""exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_regex=\d\d:\d\d\s+({host}[^\s]+)\s([^\s]+\s)?[^\s]+\[\d+\]"""
"""exa_json_path=$.host.name,exa_field_name=host"""
"""exa_json_path=$.message,exa_regex=\s01490\d+:5:.*?({session_id}[^\s:]+): (Username|Retry)"""
"""exa_json_path=$.message,exa_regex=\sUsername\s+'\s*(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*'"""
]
ParserVersion = "v1.0.0"


}
```