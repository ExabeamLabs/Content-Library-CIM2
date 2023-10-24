#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-app-activity-success-system
  ParserVersion = "v1.0.0"
  Conditions = [ """|Fortinet|Fortigate|""", """|event:system""", """FTNTFGTsubtype=system""" ]
  Fields = ${DLFortinetParsersTemplates.fortinet-network-info.Fields} [
    """act=({action}[^=]+?)\s\w+=""",
    """outcome=({result}[^=]+?)\s\w+="""
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