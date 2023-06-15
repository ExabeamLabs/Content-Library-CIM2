#### Parser Content
```Java
{
Name = barracuda-firewall-str-app-notification-success-4006
  ParserVersion = v1.0.0
  Conditions = [ """/box_Event_event""", """|Firewall|4006|""", """ Info """, """Insert Event from""", """Pending connection limit""" ]
  Fields = ${BarracudaParserTemplates.barracuda-network-info.Fields} [
    """({event_name}Pending connection limit \(\d+\) exceeded) \(\d+\) for ({protocol}[^\s]+)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)[^@]+?->\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)(-({rule}[^\)]+))?""",
  ]

barracuda-network-info = {
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """Info\s+({host}[^\s]+)""",
    """\|(F|f)irewall\|({event_code}\d+)\|"""
  
}
```