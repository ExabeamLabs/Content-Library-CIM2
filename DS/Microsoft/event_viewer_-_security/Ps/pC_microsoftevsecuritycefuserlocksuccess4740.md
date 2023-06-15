#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Microsoft-Windows-Security-Auditing:4740|"""
]
Fields = [
"""({event_name}A user account was locked out)"""
"""\sexternalId=({event_code}\d+)"""
"""\srt=({time}\d{13})"""
"""\sshost=({src_host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssntdom=({src_domain}[^\s]+)"""
"""\ssuser=({src_user}.+?)\s+\w+="""
"""\sdntdom=({domain}[^\s\\]+)"""
"""\sduser=({user}.+?)\s+\w+="""
"""\sduid=({login_id}[^\s]+)"""
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdvchost=({host}[^\s]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```