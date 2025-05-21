#### Parser Content
```Java
{
Name = "trendmicro-officescan-str-alert-trigger-success-virus"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""Virus/Malware:"""
"""Date/Time:"""
]
Fields = [
"""Computer:\s+({host}[^\s]+)\s"""
"""Date\/Time:\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)"""
"""Virus/Malware:\s({alert_name}[^\s]+)\s"""
"""Computer:\s+({src_host}[^\s]+)\s"""
"""IP address:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
"""File:\s+({malware_url}.+?)\s+Date"""
"""User name:\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```