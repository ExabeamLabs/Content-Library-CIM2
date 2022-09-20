#### Parser Content
```Java
{
Name = barracuda-firewall-str-alert-trigger-insertevent
  ParserVersion = v1.0.0
  Conditions = [ """/box_Event_event""", """|Firewall|4014|""", """ Info """, """Insert Event from""" ]
  Fields = ${BarracudaParserTemplates.barracuda-network-info.Fields} [
    """({event_name}Interface mismatch):[^\)]+? for ({protocol}[^\s]+)\s({src_ip}[a-fA-F\d:.]+?)(:({src_port}\d+))?\s[^@]+?->\s({dest_ip}[a-fA-F:.\d]+?)(:({dest_port}\d+))?(\s|-)"""
  ]

barracuda-network-info = {
  Vendor = Barracuda
  Product = Barracuda FW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """Info\s+({host}[^\s]+)""",
    """\|(F|f)irewall\|({event_code}\d+)\|"""
  
}
```