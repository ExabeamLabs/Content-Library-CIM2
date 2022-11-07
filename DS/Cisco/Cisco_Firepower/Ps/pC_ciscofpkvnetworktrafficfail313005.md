#### Parser Content
```Java
{
Name = cisco-fp-kv-network-traffic-fail-313005
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """-313005""", """%FTD-""", """error message:""" ]
  Fields = [
    """({host}[\w+\.-]+)\s+(\S*:\s*)?%FTD-\d+-\d+:""",
    """%FTD-({priority}\d+)-({event_code}\d+):\s*({event_name}.*?)\sfor\s*({protocol}\w+)\s""",
    """\ssrc\s*({src_interface}[\w-]+):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))(\(({domain}[^\\]+)\\({user}[^\\]+?)\))?""",
    """\sdst\s*({dest_interface}[\w-]+):(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)(\s|$))""",
  ]


}
```