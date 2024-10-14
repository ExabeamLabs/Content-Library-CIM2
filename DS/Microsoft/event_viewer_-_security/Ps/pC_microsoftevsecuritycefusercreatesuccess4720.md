#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-create-success-4720"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
"""|Microsoft|Microsoft Windows|""",
"""|Microsoft-Windows-Security-Auditing:4720"""
  ]
  Fields = [
"""({event_name}A user account was created)""",
"""({event_code}4720)""",
"""\srt=({time}\d{13})""",
"""\ssntdom=({domain}[^\s]+)""",
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
"""\ssuid=({login_id}[^\s]+)""",
"""\sdntdom=({account_domain}[^\s]+)""",
"""\sduser=({account_name}.+?)\s+\w+=""",
"""\sdvchost=({host}[\w\-.]+)""",
"""ad.New_,Account:Security_,ID=({account_id}[^\s]+)"""
  ]
  DupFields = [ "account_name->dest_user", "account_domain->dest_domain" ]


}
```