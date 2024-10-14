#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-success-528"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""EvntSLog"""
"""(528)"""
]
Fields = [
"""({event_name}Successful Logon)"""
"""\s+({time}\w+ \d+ \d+:\d+:\d+ \d+):.+?/Security\s+\(({event_code}\d+)\)"""
"""Successful Logon:\s+User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Domain:\s+({domain}[\w.\-]+)\s+Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
"""Logon Type:\s+({login_type}\d+)"""
"""Logon Process:\s+({auth_process}.+?)\s+Authentication Package:\s+({auth_package}[^\s]+)"""
"""Workstation Name:\s+({src_host_windows}[\w.\-\$]+)"""
"""Workstation Name:\s+({src_host}[\w.\-\$]+).*?Source Network Address:\s*-\s+"""
"""Workstation Name:\s+({dest_host}[\w.\-\$]+)"""
"""Caller User Name:\s+({account}[\w.\-\$]+)"""
"""Source Network Address:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"dest_host->host"
]
ParserVersion = "v1.0.0"


}
```