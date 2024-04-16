#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-419002
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-419002""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)""",
    """(-|({host}[\w\.-]+))\s*%ASA-|\s+(::ffff:)?({=host}[\w\.-]+)\s*:\s*%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """-419002:\s*({event_name}.*?) from """,
    """({protocol}[^\s]+)\s+SYN\s+from\s+({src_interface}.+?):(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))(\/({src_port}\d+)\s+)""",
    """\sto\s+({dest_interface}.+?):(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+))|\s+)""",
    """ with ({result_reason}.*?)\s*$"""
  ]


}
```