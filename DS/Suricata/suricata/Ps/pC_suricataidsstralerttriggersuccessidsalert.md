#### Parser Content
```Java
{
Name = "suricata-ids-str-alert-trigger-success-idsalert"
Vendor = "Suricata"
Product = "Suricata"
TimeFormat = "MM/dd/yyyy-HH:mm:ss.SSSSSS"
Conditions = [
"""[Classification:"""
""" IDS-alert """
]
Fields = [
"""\s({host}[\w]+)\sIDS-alert\s({time}\d\d\/\d\d\/\d\d\d\d-\d\d:\d\d:\d\d.\d+)"""
"""\[(?:[*]+|({additional_info}[^"\]]+))\] ({alert_name}.+?)[\s\[\]]*\[Classification:\s*({alert_type}[^\]]+)\] \[Priority:\s*({alert_severity}[^\]]+)\] \{({protocol}[^\}]+)\} ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+) -> ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```