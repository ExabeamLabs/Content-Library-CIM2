#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-enable-success-4722-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|McAfee|ESM"""
"""43-26304722"""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})(\s|0\||$)"""
"""\ssrc=({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?))(:({dest_port}\d+))?(\s|0\||$)"""
"""\sshost=({host}({dest_host}[\w\-.]+?))(\s|0\||$)"""
"""\ssntdom=({domain}[^\s]+?)(\s|0\||$)"""
"""\sdntdom=({dest_domain}[^\s]+?)(\s|0\||$)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|0\||\s*$)"""
"""\sduser=({dest_user}.+?)(\s+\w+=|0\||\s*$)"""
"""\snitroSource_Logon_ID=({login_id}.+?)(\s|0\||$)"""
]
ParserVersion = "v1.0.0"


}
```