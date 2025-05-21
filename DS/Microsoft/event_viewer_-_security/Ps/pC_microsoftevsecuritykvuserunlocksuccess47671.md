#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-unlock-success-4767-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = ["""|Microsoft-Windows-Security-Auditing:4767|""","""|A user account was unlocked""", """CEF:""" ]
Fields = [
   """Microsoft-Windows-Security-Auditing:({event_code}4767)""",
   """start=({time}\d{13})""",
   """({event_name}A user account was unlocked)""",
   """sntdom=({domain}[^=]+)\s\w+=""",
   """\ssuser=(N\/A|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+=""",
   """\ssuid=(N\/A|-|({user_uid}.+?))\s*\w+=""",
   """dhost=({host}[\w\-.]+)"""
   """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
   """duser=({dest_user}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```