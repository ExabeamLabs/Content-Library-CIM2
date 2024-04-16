#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-userlockedout"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""|user-locked-out|"""
"""Sales Cloud"""
]
Fields = [
"""destinationServiceName =({host}[\w\-\.]+)\s*(\w+=|$)""",
"""LoginTime\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
"""suser=([^\s\\\=]+\\\=)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
"""([^\|]*\|){5}({operation}[^\|]+)""",
"""SourceIp\\=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""dvchost=({src_host}[\w\-.]+)""",
"""sourceDnsDomain=({dest_host}[\w\-.]+)""",
"""\Wmsg=({additional_info}.+?)\s+(\w+=|$)""",
"""\Wduser=({object}.+?)\s+(\w+=|$)""",
"""({app}Sales Cloud)""",
"""Browser\\*=(Unknown|({browser}[^"=]+?))(;|"|\s\w+)"""
]
ParserVersion = "v1.0.0"


}
```