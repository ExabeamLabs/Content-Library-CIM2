#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-success-540"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Security:540|"""
]
Fields = [
"""({event_name}Successful Network Logon)"""
"""({event_code}540)"""
"""\srt=({time}\d{13})"""
"""\ssproc=({auth_process}.+?)\s+\w+="""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sduid=\([^,]+,({login_id}[^\)]+)"""
"""\scn1=({login_type}\d+)"""
"""\sdvchost=({host}({dest_host}[\w\-\.]+))"""
""" dntdom=({domain}[^\s]+)"""
""" src=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```