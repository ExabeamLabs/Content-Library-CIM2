#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4769-9"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304769"""
]
Fields = [
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""({event_name}A Kerberos service ticket was requested)"""
"""\srt=({time}\d{13})"""
"""shost=({host}[^\s]+)"""
"""nitroCommandID=({result_code}.+?)\s+\w+="""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""nitroService_Name =({dest_host}\S+\$)\s"""
"""nitroService_Name =({service_name}\S+)"""
"""sntdom=({domain}[^\s]+)"""
"""suser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"


}
```