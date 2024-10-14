#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-success-528-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""MSWinEventLog"""
""",528,"""
"""Security"""
"""Successful Logon:"""
"""rsa_sa_log"""
]
Fields = [
"""({event_name}Successful Logon)"""
"""(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+),"""
"""\d{2}:\d{2}:\d{2} \d{4},({event_code}[^,]+),Security"""
"""Security,({event_id}\d+)"""
"""User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+\([^,\s]+[,\s]({login_id}[^\)]+)\)\s+Logon Type:\s+({login_type}\d+)"""
"""Logon Process:\s+({auth_process}.+?)\s+Authentication Package:\s+({auth_package}[^\s]+)"""
"""Source Network Address:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```