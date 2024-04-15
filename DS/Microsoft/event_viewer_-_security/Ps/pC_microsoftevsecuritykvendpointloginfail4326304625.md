#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-4326304625"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304625"""
]
Fields = [
"""({event_name}An account failed to log on)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})"""
"""deviceTranslatedAddress=({host}[a-fA-F:\d.]+)"""
"""sntdom=({domain}[^\s]+)"""
"""suser=({user}.+?)\s+\w+="""
"""dst=(?:-|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+\w+="""
"""src=(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
"""nitroAppID=({auth_package}[^\s]+)"""
"""nitroLogon_Type=({login_type}\d+)"""
"""nitroMessage_Text=({result_code}[^\s]+)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```