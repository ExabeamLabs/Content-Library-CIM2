#### Parser Content
```Java
{
Name = citrix-appfw-str-network-traffic-400-resp
  ParserVersion = v1.0.0
  Product = Citrix Web App Firewall
  Vendor = Citrix
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ APPFW """, """PPE""", """ AF_400_RESP """ ]
  Fields = [
    """\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({alert_name}({event_name}\S+))\s+({event_code}\S+)""",
    """\s\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s+(\S+\s+){9}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+({alert_id}\S+)""",
    """\s\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s+(\S+\s+){12}({rule}\S+)\s+({url}[^\s]+)\s+({result}[^<]+)\s+<({action}[^>]+)>""",
    """APPFW.*?:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+({alert_id}\S+)\s+\S+\s+({rule}\S+)\s+({url}[^\s]+)\s+({failure_reason}[^<]+?)\s*<blocked>"""
  ]


}
```