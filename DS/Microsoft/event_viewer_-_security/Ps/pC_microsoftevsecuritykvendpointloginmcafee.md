#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-mcafee"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304770"""
]
Fields = [
"""({event_name}A Kerberos service ticket was renewed)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})\s+cnt"""
"""shost=({host}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""sntdom=({domain}[^\s]+)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""nitroAppID=({dest_host}[\w\-.]+)"""
"""nitroAppID=({service_name}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```