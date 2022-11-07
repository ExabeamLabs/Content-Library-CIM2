#### Parser Content
```Java
{
Name = huawei-usg-kv-app-notification-success-sec
  ParserVersion = "v1.0.0"
  Conditions = [ """SEC/""", """%%""", """/STREAM""" ]
  Fields = ${HUAWEILMSParserTemplates.huawei-ids-2.Fields}[
    """%%[^:]*?:\s*({event_name}.+?)\s*$"""
  ]

huawei-ids-2 {
  Vendor = Huawei
  Product = Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """:\d\d\s({host}[^\s]+)\s*%""",
     """PeerAddress=({dest_ip}[^,]+)""",
     """PeerPort=({dest_port}\d+)""",
     """Reason=({policy_name}[^)]+)""",
     """:\s*({event_name}[^:\/]+)\.\s*\(""",
     """Destination address:\s*({dest_ip}[^,]+)"""
  
}
```