#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-success-528"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-21100528"""
]
Fields = [
"""({event_name}Successful Logon)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})"""
"""shost=({host}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""sntdom=({domain}[^\s]+)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+nitro[\w]+="""
"""nitroLogon_Type=({login_type}\d+)"""
"""nitroDestination_Logon_ID=\([^,]+,({login_id}[^\)]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```