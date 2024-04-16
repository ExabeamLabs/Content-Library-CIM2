#### Parser Content
```Java
{
Name = "microsoft-nps-csv-endpoint-authentication-success-wirelessconnection"
Vendor = "Microsoft"
Product = "Microsoft Network Policy Server"
TimeFormat = "MM/dd/yyyy,HH:mm:ss"
Conditions = [
  """,IAS,"""
  """,4136,1,4142,0"""
]
Fields = [
  """,({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d),IAS,({auth_server}[^\,]+),""",
  """,4130,(({domain}[^\\\s']+)[\\]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?)),""",
  """,4127,({auth_type}\d+),""",
  """,({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),4116,""",
  """,25,\d+\s+\d+\s+({host}[^\s]+)\s""",
  """,30,[^:]+\:({network}[^\,]+),""",
  """,31,({src_mac}([a-fA-F\d]{0,2}[-:]){0,5}[a-fA-F\d]+),"""
]
ParserVersion = "v1.0.0"


}
```