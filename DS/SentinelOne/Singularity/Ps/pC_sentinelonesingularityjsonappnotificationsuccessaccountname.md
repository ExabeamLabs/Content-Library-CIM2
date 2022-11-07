#### Parser Content
```Java
{
Name = sentinelone-singularity-json-app-notification-success-accountname
  Vendor = SentinelOne
  Product = Singularity
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """totalMemory"""" ,"""accountName"""", """"s1domain": """"]
  Fields = [
    """"_time":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""",
    """"computerName":\s*"({computer_name}[^"]+)""""
    """"inet":\s*\["({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"]""",
    """"accountName":\s*"({account}[^"]+)"""",
    """"domain":\s*"({domain}[^"]+)"""",
    """"accountId":\s*"({account_id}\d+)"""",
    """"osType":\s*"({os}[^"]+)""""
  ]


}
```