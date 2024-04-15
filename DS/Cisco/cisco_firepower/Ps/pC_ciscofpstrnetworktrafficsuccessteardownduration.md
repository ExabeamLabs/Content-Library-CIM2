#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-teardown-duration"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """%FTD-"""
    """-30201"""
    """: Teardown """
    """ duration """
  ]
  Fields = [
    """({host}[\w\-.]+)\s*:\s*%FTD-"""
    """%FTD-({priority}\d+)-({event_code}\d+)"""
    """({event_name}Teardown ({protocol}\w+) connection)"""
    """\sconnection\s+({connection_id}\d+)"""
    """\sfor\s+({src_interface}.+?):({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)\/({src_port}\d+)"""
    """\sto\s+({dest_interface}.+?):({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)\/({dest_port}\d+)"""
    """\sduration\s+({duration}\S+)\s+bytes\s+({bytes}\d+)(\s+({reason}[^\(]+[^\(\s]))?(\s+\((({email_address}[^@\)]+@[^\.\)]+\.[^\)]+)|({user}[^@\)]+]))\))?""",
    """%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(({email_address}[^@\)]+@[^\.\)]+\.[^\)]+)|({user}[^\\\/\)]+?))\)"""
  ]
  DupFields = [
    "event_name->operation"
  ]


}
```