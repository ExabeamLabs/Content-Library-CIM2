#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-switch-success-4648-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304648"""
]
Fields = [
"""({event_name}A logon was attempted using explicit credentials)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})"""
"""deviceTranslatedAddress=({host}[a-fA-F:\d.]+)"""
"""deviceExternalId=({host}[^\s]+)"""
"""shost=({dest_host}[\w\-.]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""duser=({account}({dest_user}[\w\-\.]+(?:\w+)?\$?))\s+suser"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+nitroSecurity"""
"""sntdom=({domain}.+?)\s+shost"""
"""nitroSecurity_ID=({user_sid}[^\s]+)"""
"""nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
"""nitroAppID=\s*(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```