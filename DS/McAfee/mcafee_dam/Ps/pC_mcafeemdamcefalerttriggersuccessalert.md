#### Parser Content
```Java
{
Name = mcafee-mdam-cef-alert-trigger-success-alert
  Vendor = McAfee
  Product = McAfee DAM
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|McAfee|DAM|""", """|alert|""", """externalId=""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wcs1=MSSQL:({host}[\w\-.]+)""",
    """\WexternalId=({alert_id}\d+)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wduser=((|NT AUTHORITY|({domain}[^\\\s]+))\\+)?(|SYSTEM|({user}[^\\\s]+))\s+(\w+=|$)""",
    """\Wsuser=((|NT AUTHORITY|({domain}[^\\\s]+))\\+)?(|SYSTEM|({user}[^\\\s]+))\s+(\w+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wact=({alert_type}.+?)\s+(\w+=|$)""",
    """\Wcs2=\s*({additional_info}.+?)\s+(\w+=|$)""",
    """\|alert\|({alert_name}[^\|]+)""",
  ]


}
```