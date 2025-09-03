#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-106001
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-106001""", """denied """ ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
    """({event_name}Inbound ({protocol}\w+) connection ({result}denied))"""
    """\sfrom\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)\s+to\s+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)\s""",
    """ on interface(\s+({dest_interface}\S+))?"""
    """\d\d:\d\d:\d\d\s+(::ffff:)?((?i)system|({host}[\w\.-]+))[\s:]+%ASA-"""
  ]
  DupFields = ["event_name->failure_reason"]


}
```