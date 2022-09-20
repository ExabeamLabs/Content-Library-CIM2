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
"""\srt=({time}\d+)"""
"""\sshost=({src_host}[^\s]+)"""
"""\ssrc=({src_ip}[a-fA-F:\d.]+)"""
"""\ssntdom=({domain}[^\s]+)"""
"""\ssuser=({user}.+?)\s+\w+="""
"""\sdntdom=({domain}[^\s\\]+)"""
"""\sduser=({dest_user}.+?)\s+\w+="""
"""\sduid=({login_id}[^\s]+)"""
"""\sdvc=({dest_ip}[a-fA-F:\d.]+)"""
"""\sdvchost=({host}[^\s]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```