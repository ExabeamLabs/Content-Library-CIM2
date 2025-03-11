#### Parser Content
```Java
{
Name = cisco-asa-str-ssl-traffic-725003
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ 
  """-725003"""
  """%ASA-"""
  ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d).*?%ASA-({priority}\d+)"""
    """({event_code}725003)"""
    """({event_name}request to resume previous session)"""
    """({src_interface}[^\s]+):(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+))\/({src_port}\d+)"""
    """to\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+))\/({dest_port}\d+)"""
    """\s(::ffff:)?(-|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]


}
```