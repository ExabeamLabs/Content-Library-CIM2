#### Parser Content
```Java
{
Name = mcafee-mdam-cef-alert-trigger-success-alert
  Vendor = McAfee
  Product = MDAM
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|McAfee|DAM|""", """|alert|""", """externalId=""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wcs1=MSSQL:({host}[\w\-.]+)""",
    """\WexternalId=({alert_id}\d+)""",
    """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wduser=((|NT AUTHORITY|({domain}[^\\\s]+))\\+)?(|SYSTEM|({user}[^\\\s]+))\s+(\w+=|$)""",
    """\Wsuser=((|NT AUTHORITY|({domain}[^\\\s]+))\\+)?(|SYSTEM|({user}[^\\\s]+))\s+(\w+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wact=({alert_type}.+?)\s+(\w+=|$)""",
    """\Wcs2=\s*({additional_info}.+?)\s+(\w+=|$)""",
    """\|alert\|({alert_name}[^\|]+)""",
  ]


}
```