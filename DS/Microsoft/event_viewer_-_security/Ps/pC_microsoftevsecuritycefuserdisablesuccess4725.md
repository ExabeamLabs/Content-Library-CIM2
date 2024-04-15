#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-disable-success-4725"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Microsoft-Windows-Security-Auditing:4725|"""
]
Fields = [
"""({event_name}A user account was disabled)"""
"""\sexternalId=({event_code}\d+)"""
"""\srt=({time}\d{13})"""
"""\sdvc=({host}[a-fA-F:\d.]+)"""
"""\sdvchost=({host}[^\s]+)"""
"""\sdhost=({dest_host}[^\s]+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\ssuser=({user}.+?)\s+\w+="""
"""\ssntdom=({domain}.+?)\s\w+="""
"""\ssuid=({login_id}[^\s]+)"""
"""\sduser=({dest_user}.+?)\s+\w+="""
"""\sdntdom=({dest_domain}.+?)\s\w+="""
"""Security_,ID=({dest_user_sid}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```