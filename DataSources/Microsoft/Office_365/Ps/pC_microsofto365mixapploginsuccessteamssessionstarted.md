#### Parser Content
```Java
{
Name = microsoft-o365-mix-app-login-success-teamssessionstarted
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Workload""", """"Operation":"TeamsSessionStarted"""" ]
  Fields = [
    """"CreationTime":"({time}\d+\-\d+\-\d+T\d+:\d+:\d+)"""",
    """"Workload":"({app}[^"]+)"""",
    """"UserId":"({email_address}[^@]+@({email_domain}[^"]+))"""",
    """\Wsuser=({email_address}[^@]+@({email_domain}[^\s]+))\s+(\w+=|$)""",
    """"Operation":"({additional_info}[^"]+)""""
  ]


}
```