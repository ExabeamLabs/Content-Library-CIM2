#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-713228
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """Assigned private IP address""", """-713228""","""%ASA-""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d+:\d+:\d+):""",
    """%ASA-({priority}\d+)-({event_code}\d+): Group =\s*({realm}[^,]+),\s*Username = ({user}[^,@]+?),?\s+IP = ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?[,\s]+Assigned private IP address ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) to"""
  ]


}
```