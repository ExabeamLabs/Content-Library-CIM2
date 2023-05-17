#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-app-activity-success-connector
  ParserVersion = "v1.0.0"
  Conditions = [ """|Fortinet|Fortigate|""", """|event:connector|""", """FTNTFGTsubtype=connector""" ]

fortinet-network-info = {
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch_sec"
  Fields = [
    """FTNTFGTeventtime=({time}\d{10})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """\smsg=({additional_info}[^"]+?)\s*(\w+=|$)"""
  
}
```