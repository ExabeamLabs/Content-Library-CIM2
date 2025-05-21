#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-lock-success-4800"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|Microsoft Windows|"""
"""|Microsoft-Windows-Security-Auditing:4800|"""
]
Fields = [
"""({event_name}The workstation was locked)"""
"""\sexternalId=({event_code}\d+)"""
"""\srt=({time}\d{13})"""
"""\sdvc=({host}[a-fA-F:\d.]+)"""
"""\sdvchost=({host}[^\s]+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdhost=({dest_host}[\w\-.]+)"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sdntdom=({domain}[^\s]+)"""
"""\sduid=({login_id}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```