#### Parser Content
```Java
{
Name = "lumension-l-csv-peripheral-storage-activity-fail-writedenied-1"
Vendor = "Lumension"
Product = "Lumension"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""","WRITE-DENIED",""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)","[^"]*","(({domain}[^"\\\/]+)[\\\/]+)?({user}[^"\\\/]+)?","({user_ou}[^"]+)","({operation}WRITE-DENIED)","({host}[^"]+)",("[^"]*",){2}"({file_path}[^"]+)",""""
""","({process_name}[^"]+)"\s*$"""
]
ParserVersion = "v1.0.0"


}
```