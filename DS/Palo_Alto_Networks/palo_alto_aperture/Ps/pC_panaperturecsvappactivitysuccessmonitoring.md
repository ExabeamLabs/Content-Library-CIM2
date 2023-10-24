#### Parser Content
```Java
{
Name = "pan-aperture-csv-app-activity-success-monitoring"
Vendor = "Palo Alto Networks"
Product = "Palo Alto Aperture"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""activity_monitoring"""
""" Aperture """
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s({host}[^\s]+)"""
"""activity_monitoring,\"?({app}[^,\"]+)"""
"""activity_monitoring,\"*([^,]*,){5}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),"""
""",activity_monitoring,([^,]*,){4}\"*([\w\s]+|({email_address}[^@]+@[^\",]+))\"*,({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```