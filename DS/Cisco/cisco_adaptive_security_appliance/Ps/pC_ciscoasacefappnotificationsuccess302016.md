#### Parser Content
```Java
{
Name = cisco-asa-cef-app-notification-success-302016
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  Conditions = [ """CEF:""", """|CISCO|ASA||302016|Teardown UDP connection|""" ]

cef-cisco-network-connection = {
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "epoch"
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)\|({priority}[^\|]+)""",
    """\WeventId=({event_code}\d+)""",
    """\Wproto=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d{13})""",
    """\Wsrc=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wdst=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wdvc=(|(::ffff:)?({host}.+?))(\s+\w+=|\s*$)""",
    """\WdeviceDirection=(|({direction}.+?))(\s+\w+=|\s*$)""",
  
}
```