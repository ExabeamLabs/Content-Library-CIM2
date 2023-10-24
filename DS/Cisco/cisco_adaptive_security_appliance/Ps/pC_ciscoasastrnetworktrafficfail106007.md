#### Parser Content
```Java
{
Name = "cisco-asa-str-network-traffic-fail-106007"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-106007""", """Deny """ ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}({action}Deny).+?\s+({protocol}\w+))""",
    """\sfrom\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)\s+to\s+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)\s""",
  ]


}
```