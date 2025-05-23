#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-fail-106015
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ """%ASA-""", """-106015""", """Deny TCP""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w+ \d{1,2} (\d\d\d\d )?\d\d:\d\d:\d\d)""",
    """(-|({host}[\w\.-]+))\s*%ASA-|\s+(::ffff:)?({=host}[\w\.-]+)\s*:\s*%ASA-""",
    """%(asa|ASA)-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Deny ({protocol}TCP) \(({result_reason}[^\)]*)\))""",
    """\sfrom\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)""",
    """\sto\s+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)""",
    """\sflags\s+(.+?)\s+on interface\s+({interface}\S+)""" # flags is removed,
  ]


}
```