#### Parser Content
```Java
{
Name = cisco-asa-str-ip-assign-737026
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-737026""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """({event_name}Client assigned)""",
    """Client assigned (({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))"""
  ]


}
```