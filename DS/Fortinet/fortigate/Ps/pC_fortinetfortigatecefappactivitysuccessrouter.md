#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-app-activity-success-router
  ParserVersion = "v1.0.0"
  Conditions = [ """|Fortinet|Fortigate|""", """|event:router|""", """FTNTFGTlogdesc=""" ]
  Fields = ${DLFortinetParsersTemplates.fortinet-network-info.Fields} [
    """: From ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? via """
  ]

fortinet-network-info = {
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch_sec"
  Fields = [
    """FTNTFGTeventtime=({time}\d{10})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """\smsg=({additional_info}[^"]+?)\s*(\w+=|$)""",
    """\Wtz="?({tz}[+-]\d+)"""
  
}
```