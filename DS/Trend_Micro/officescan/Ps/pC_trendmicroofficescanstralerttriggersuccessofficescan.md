#### Parser Content
```Java
{
Name = "trendmicro-officescan-str-alert-trigger-success-officescan"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""OfficeScan"""
"""Virus found action result"""
]
Fields = [
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""result\s+\d{1,2}/\d{1,2}/\d{4} \d{1,2}:\d{2}:\d{2} \w{2}\s+.+[AP]M\s+[^\s]+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+?\s({alert_name}OfficeScan)\s+[^\s]+\s+({alert_type}\w+)\s+[^\s]+\s+[^\s]+\s+[^\s]+\s+[^\s]+\s+[^\s]+\s+({src_host}[^\s]+)"""
]
DupFields = [
"src_host->host"
]
ParserVersion = "v1.0.0"


}
```