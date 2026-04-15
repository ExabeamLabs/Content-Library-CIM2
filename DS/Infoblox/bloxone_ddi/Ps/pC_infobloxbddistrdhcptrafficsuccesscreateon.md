#### Parser Content
```Java
{
Name = "infoblox-bddi-str-dhcp-traffic-success-createon"
    ParserVersion = "v1.0.0"
    Vendor = Infoblox
    Product = BloxOne DDI
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """ dhcp[""", """Create on""", """fingerprint lifetime""" ]
    Fields = [
        """\s*({host}[\w.-]+)\s*\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}Z""",
        """dhcp\[({process_id}\d+)\]:\s*({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}Z)\s*({src_host}[\w.-]+):\s*({operation}Create) on\s*({src_ip}(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?))\s*to\s*({src_mac}(?:[0-9A-Fa-f]{2}[:-]){5}(?:[0-9A-Fa-f]{2}))\s*fingerprint lifetime\s*({lease_time}\d+)"""
    ]


}
```