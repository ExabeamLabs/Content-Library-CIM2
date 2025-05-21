#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-305006
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """-305006""", """%ASA-""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d):\s*""",
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)""",
    """%ASA-({priority}\d+)""",
    """({event_code}305006)""",
    """({event_name}regular translation creation failed) for ({protocol}\w+) src ({src_interface}\S+?)\s*:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(\(({domain}[^\\\/\s]+)[\\\/]({src_host}[^\\\/\s]+)\))? dst ({dest_interface}\S+?)\s*:\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))"""
  ]


}
```