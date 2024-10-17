#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-authentication-success-dsepamauth"
Vendor = "Unix"
Product = "Unix"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
Conditions = [
"""(dsepam:auth):"""
"""authentication success;"""
]
Fields = [
"""({time}\w+ \d+ \d\d:\d\d:\d\d)\s+({host}\S+)\s+\S+\s+\S+\(dsepam:auth\)"""
"""\suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```