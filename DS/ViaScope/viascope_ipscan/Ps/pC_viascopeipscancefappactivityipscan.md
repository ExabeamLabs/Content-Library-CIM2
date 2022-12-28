#### Parser Content
```Java
{
Name = viascope-ipscan-cef-app-activity-ipscan
  Vendor = ViaScope
  Product = ViaScope IPScan
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = ["""|ViaScope""" , """|IPScan"""]
  Fields = [
     """\srt=({time}\d{13})"""
     """dvc=({host}[^\s]+)""",
     """dvchost=({host}[^\s]+)""",
     """IPScan[^|]+?\|[^|]+?\|({event_name}[^\|]+)""",
     """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """eventId=({event_code}[^\s]+)"""
  ]


}
```