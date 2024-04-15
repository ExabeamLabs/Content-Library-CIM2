#### Parser Content
```Java
{
Name = "pan-aperture-kv-alert-trigger-success-incident"
Vendor = "Palo Alto Networks"
Product = "Palo Alto Aperture"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" Aperture """
""",incident,"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s({host}[\w\-.]+)\s"""
"""incident,\"*({app}[^\",]+)\",({alert_severity}\d(\.\d)?)\"*,({alert_id}[\dA-Fa-f]+)\"*\"*,"""
"""\d+:\d+Z,([^,]*,){3}\"?({email_address}[^@]+@[^\.]+[^,\"]+)"""
"""\"+({alert_name}[^\"]+)\"+,EXTERNAL,"""
""",incident,\"?({alert_type}[^\",]+)"""
"""incident,\"*({app}[^\",]+)\",({alert_severity}\d(\.\d)?)\"*,({alert_id}[\dA-Fa-f]+)\"*,[\dA-Fa-f]+\"*,\"*\s*({additional_info}[^,\s\"]+)\s*\"*,([^,]*,)"""
]
ParserVersion = "v1.0.0"


}
```