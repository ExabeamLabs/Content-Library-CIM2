#### Parser Content
```Java
{
Name = barracuda-firewall-str-app-notification-success-4006
  ParserVersion = v1.0.0
  Conditions = [ """/box_Event_event""", """|Firewall|4006|""", """ Info """, """Insert Event from""", """Pending connection limit""" ]
  Fields = ${BarracudaParserTemplates.barracuda-network-info.Fields} [
    """({event_name}Pending connection limit \(\d+\) exceeded) \(\d+\) for ({protocol}[^\s]+)\s({src_ip}[a-fA-F\d:.]+?):({src_port}\d+)[^@]+?->\s({dest_ip}[a-fA-F\d:.]+?):({dest_port}\d+)(-({rule}[^\)]+))?""",
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