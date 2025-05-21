#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-app-notification-success-accountname
  Vendor = SentinelOne
  Product = Singularity Platform
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """totalMemory"""" ,"""accountName"""", """"s1domain": """"]
  Fields = [
    """"_time":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""",
    """"computerName":\s*"({computer_name}[^"]+)""""
    """"inet":\s*\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"]""",
    """"accountName":\s*"({account}[^"]+)"""",
    """"domain":\s*"({domain}[^"]+)"""",
    """"accountId":\s*"({account_id}\d+)"""",
    """"osType":\s*"({os}[^"]+)""""
  ]


}
```