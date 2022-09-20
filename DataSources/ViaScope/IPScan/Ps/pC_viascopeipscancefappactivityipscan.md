#### Parser Content
```Java
{
Name = viascope-ipscan-cef-app-activity-ipscan
  Vendor = ViaScope
  Product = IPScan
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = ["""|ViaScope""" , """|IPScan"""]
  Fields = [
     """\srt=({time}[^\s]+)"""
     """dvc=({host}[^\s]+)""",
     """dvchost=({host}[^\s]+)""",
     """IPScan[^|]+?\|[^|]+?\|({event_name}[^\|]+)""",
     """\ssrc=({src_ip}[^\s]+)"""
     """eventId=({event_code}[^\s]+)"""
  ]


}
```