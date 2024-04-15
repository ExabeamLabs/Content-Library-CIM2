#### Parser Content
```Java
{
Name = "citrix-appfw-str-network-traffic-bufferoverflowcookie"
  ParserVersion = "v1.0.0"
  Product = "Citrix Web App Firewall"
  Vendor = "Citrix"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [
""" APPFW """
"""PPE"""
""" APPFW_BUFFEROVERFLOW_COOKIE """
  ]
  Fields = [
"""\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({event_name}\S+)\s+({event_code}\S+)\s+\d+\s+:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+({alert_id}\S+)\s+\S+\s+({result}[^:]+?)\s*:\s+({url}[^\s]+)\s+<({action}[^>]+)>"""
  ]
  DupFields = [
"event_name->alert_name"
  ]


}
```