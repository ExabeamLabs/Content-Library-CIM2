#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-app-activity-dlpclassification
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions= [ """destinationServiceName =Office 365""", """flexString1=DlpClassification""" ]
  Fields = [
    """"CreationTime\\*"+:\\*\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """\WflexString1=({operation}.+?)\s+(\w+=|$)""",
    """\Wsuser=(({email_address}[^\s@]+@[^\s@]+)|({user}[^\s]+?))\s+(\w+=|$)""",
    """"UserId":"(({email_address}[^\s@]+@[^\s@]+)|({user}[^\s]+?))"+"""
    """"FileName":"({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""",
    """"FilePathUrl":"({file_path}({file_dir}[^"]*[\\\/]+)[^\\\/"]*)"""",
    """"FileOwner":"({last_name}[^",]+),\s*({first_name}[^",]+)"""",
    """"Workload":"({app}[^"]+)"""",
    """"Operation":"({event_name}[^"]+)"""",
  ]


}
```