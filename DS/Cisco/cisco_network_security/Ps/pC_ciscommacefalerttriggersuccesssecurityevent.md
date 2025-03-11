#### Parser Content
```Java
{
Name = "cisco-mma-cef-alert-trigger-success-securityevent"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "epoch_sec"
Conditions = [
  """security_event"""
  """ids_alerted"""
  """timestamp="""
]
Fields = [
  """\s({host}[\w.\-]+)\s+(\S+\s+){2}security_event"""
  """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)"""
  """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)"""
  """\sprotocol=({protocol}\w+)"""
  """\ssignature=({alert_type}\S+)"""
  """\spriority=({alert_severity}\d+)"""
  """\stimestamp=({time}\d{10})"""
  """\sdirection=({direction}\S+)"""
  """\smessage:\s*({alert_name}({alert_type}[^\s]+).+?)\s*$"""
  """\sdhost=(({dest_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({dest_host}[\w\-\.]+))"""
  """\sshost=(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_host}[\w\-\.]+))"""
]
ParserVersion = "v1.0.0"


}
```