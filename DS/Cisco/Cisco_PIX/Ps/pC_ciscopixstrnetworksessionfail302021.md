#### Parser Content
```Java
{
Name = cisco-pix-str-network-session-fail-302021
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco PIX
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%PIX""" , """-302021""", """Teardown """,""" faddr """ ]
  Fields = [
    """({time}\w+\s\d+\s\d+\s\d+:\d+:\d+)\s+({host}[^\s]+)""",
    """%PIX-({priority}\d+)-({event_code}\d+)""",
    """({event_name}({action}Teardown)\s+({protocol}\w+))""",
    """faddr\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
    """gaddr\s({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?"""
    ]


}
```