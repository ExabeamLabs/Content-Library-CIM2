#### Parser Content
```Java
{
Name = "adaxes-a-str-app-activity-success-adaxes"
Vendor = "Adaxes"
Product = "Adaxes"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
Conditions = [
""" ADAXES """, """|Add""", """|Success"""
]
Fields = [
""""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""\s\d\d\:\d\d\:\d\d\s+({host}[\w.\-]+)\s+\S+\s+\S+\s+\d\d\:\d\d\:\d\d\s+({app}[^\s]+)\s+({full_name}[^\|\(\)]+)(\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^|]+))?\))?\|({operation}[^\(']+)\s*\(?'({object}.+?)'\)?(\s+[^\|]*?'({target}.+?)\s*')?[^\|]*\|({result}Success)?"""
"""\s+({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)"""
]
ParserVersion = "v1.0.0"


}
```