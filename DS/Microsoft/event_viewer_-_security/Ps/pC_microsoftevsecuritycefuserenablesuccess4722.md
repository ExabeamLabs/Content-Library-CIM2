#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-enable-success-4722"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Microsoft-Windows-Security-Auditing:4722"""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""\sexternalId=({event_code}\d+)"""
"""\srt=({time}\d{13})"""
"""\ssntdom=({domain}[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\ssuid=({login_id}[^\s]+)"""
"""\sdntdom=({dest_domain}[^\s]+)"""
"""\sduser=({dest_user}.+?)\s+\w+="""
"""\sdvchost=({host}[^\s]+)"""
"""\sdhost=({dest_host}[\w\-.]+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```