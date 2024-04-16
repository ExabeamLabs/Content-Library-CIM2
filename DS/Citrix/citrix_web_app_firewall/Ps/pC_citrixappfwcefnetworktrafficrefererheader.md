#### Parser Content
```Java
{
Name = "citrix-appfw-cef-network-traffic-referer-header"
  ParserVersion = "v1.0.0"
  Vendor = "Citrix"
  Product = "Citrix Web App Firewall"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MM/dd/yyyy:HH:mm:ss"]
  Conditions = [ """ APPFW """, """PPE""", """ APPFW_REFERER_HEADER """ ]
  Fields = [
"""\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({event_name}\S+)\s+({event_code}\S+)\s+\d+\s+:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+({alert_id}\S+)\s+\S+\s+({rule}\S+)\s+({url}[^\s]+)\s+({result}[^<]+?)\s*<({action}[^>]+)>"""
]
DupFields = [
"event_name->alert_name"
]


}
```