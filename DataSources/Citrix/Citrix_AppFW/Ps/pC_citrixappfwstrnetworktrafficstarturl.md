#### Parser Content
```Java
{
Name = citrix-appfw-str-network-traffic-starturl
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix AppFW
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ APPFW """, """PPE""", """ APPFW_STARTURL """ ]
  Fields = [
    """\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({event_name}\S+)\s+({event_code}\S+)\s+\d+\s+:\s+({src_ip}[A-Fa-f:\d.]+)\s+({alert_id}\S+)\s+\S+\s+({rule}\S+)\s+({result}[^:]+?)\s*:\s+({url}[^<]+)\s+<({action}[^>]+)>""",
    """APPFW.*?:\s+({src_ip}[A-Fa-f:\d.]+)\s+({alert_id}\S+)\s+\S+\s+({rule}\S+)\s+({result}[^:]+)\s*.*?<blocked>"""
  ]
  DupFields = [ "event_name->alert_name" ]


}
```