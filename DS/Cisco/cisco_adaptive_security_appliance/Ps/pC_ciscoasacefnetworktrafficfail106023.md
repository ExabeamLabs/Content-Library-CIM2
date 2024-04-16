#### Parser Content
```Java
{
Name = cisco-asa-cef-network-traffic-fail-106023
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-106023""", """Deny """, """ by access-group""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)""",
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}({result}Deny)\s+({protocol}\w+))""",
    """\ssrc\s+({src_interface}.+?):(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))(\/({src_port}\d+))?(\s|\(.*?\)\s)""",
    """\sdst\s+({dest_interface}.+?):(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))(\/({dest_port}\d+))?(\s|\(.*?\)\s)""",
    """ by access-group(\s{1,100}"{0,20}({access_group}[^\s"]{1,2000}))?"""
  ]


}
```