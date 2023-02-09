#### Parser Content
```Java
{
Name = barracuda-firewall-str-app-notification-success-4004
  ParserVersion = v1.0.0
  Conditions = [ """/box_Event_event""", """|firewall|4004|""", """ Info """, """Insert Event from""", """pending session""" ]
  Fields = ${BarracudaParserTemplates.barracuda-network-info.Fields} [
    """pending session ->\s+({event_name}[^\)]+)\)""",
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