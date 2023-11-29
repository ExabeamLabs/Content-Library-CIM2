#### Parser Content
```Java
{
Name = cisco-fp-str-network-session-fail-710003
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-710003""", """%FTD-""", """access denied by ACL""" ]
  Fields = [
    """({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*""",
    """%FTD-({priority}\d+)-({event_code}\d+)"""
    """({failure_reason}({protocol}\S+?) ({event_name}access denied by ACL))""",
    """ from ((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\/({src_port}\d+) to ({dest_interface}\S+?)\s*:\s*((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]
  DupFields = [
  "event_name->operation"
  ]


}
```