#### Parser Content
```Java
{
Name = cisco-asa-cef-network-traffic-fail-106023-1
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  Conditions = [ """CEF:""", """|CISCO|ASA||106023|A real IP packet was denied by the ACL|""" ]

cef-cisco-network-connection = {
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "epoch"
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)\|({priority}[^\|]+)""",
    """\WeventId=({event_code}\d+)""",
    """\Wproto=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d+)""",
    """\Wsrc=(::ffff:)?({src_ip}[a-fA-F\d.:]+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdst=(::ffff:)?({dest_ip}[a-fA-F\d.:]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wdvc=(|(::ffff:)?({host}.+?))(\s+\w+=|\s*$)""",
    """\WdeviceDirection=(|({direction}.+?))(\s+\w+=|\s*$)""",
  
}
```