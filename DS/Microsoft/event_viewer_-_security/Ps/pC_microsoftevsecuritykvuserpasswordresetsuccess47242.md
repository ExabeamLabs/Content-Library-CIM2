#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-reset-success-4724-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304724"""
]
Fields = [
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""({event_name}An attempt was made to reset an account's password)"""
"""\srt=({time}\d{13})"""
"""shost=({host}[^\s]+)"""
"""sntdom=({domain}[^\s]+)"""
"""dntdom=({dest_domain}[^\s]+)"""
"""suser=({user}.+?)\s+\w+="""
"""duser=({dest_user}.+?)\s+\w+="""
"""nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
"""nitroSecurity_ID=({user_sid}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```