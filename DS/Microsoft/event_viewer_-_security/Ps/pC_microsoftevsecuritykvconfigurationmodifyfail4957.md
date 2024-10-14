#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-configuration-modify-fail-4957"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = ["""|Microsoft-Windows-Security-Auditing:4957|""","""|Windows Firewall did not apply the following rule""", """CEF:""" ]
Fields = [
   """start=({time}\d{13})""",
   """Microsoft-Windows-Security-Auditing:({event_code}4957)""",
   """({event_name}Windows Firewall did not apply the following rule)""",
   """sntdom=({domain}[^=]+)\s\w+=""",
   """\ssuser=(N\/A|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+=""",
   """\ssuid=(N\/A|-|({user_uid}.+?))\s*\w+=""",
   """dhost=({host}[\w\-.]+)"""
   """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
   """duser=({dest_user}.+?)\s+\w+=""",
   """cs4=({failure_reason}[^=]+)\s\w+="""
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```