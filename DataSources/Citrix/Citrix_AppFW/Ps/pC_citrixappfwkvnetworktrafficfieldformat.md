#### Parser Content
```Java
{
Name = citrix-appfw-kv-network-traffic-fieldformat
Product = "Citrix AppFW"
Vendor = "Citrix"
TimeFormat = "MM/dd/yyyy:HH:mm:ss"
Conditions = [
  """ APPFW """
  """PPE"""
  """ APPFW_FIELDFORMAT """
]
Fields = [
  """\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(GMT|({host}\S+))\s+({interface_in}\S+)\s+:\s+(\S+\s+){2}({event_name}\S+)\s+({event_code}\S+)\s+\d+\s+:\s+({src_ip}[A-Fa-f:\d.]+)\s+({alert_id}\S+)\s+\S+\s+({rule}\S+)\s+({url}[^\s]+)\s+({result}[^<]+?)\s*<({action}[^>]+)>"""
]
DupFields = [
  "event_name->alert_name"
]
ParserVersion = "v1.0.0"


}
```