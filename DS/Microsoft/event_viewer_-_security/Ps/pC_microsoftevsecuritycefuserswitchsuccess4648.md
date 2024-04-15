#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-switch-success-4648"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
"""|Microsoft|Microsoft Windows|""",
"""|Microsoft-Windows-Security-Auditing:4648|"""
  ]
  Fields = [
"""({event_name}A logon was attempted using explicit credentials)""",
"""\sexternalId=({event_code}\d+)""",
"""\srt=({time}\d{13})""",
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
"""\sdvchost=({dest_host}[^\s]+)""",
"""\sduser=(-|({user}[^=]+?))\s+\w+=""",
"""\ssuser=(-|({user}[^=]+?))\s+\w+=""",
"""\sduser=({dest_user}.+?)\s+\w+=""",
"""\sdntdom=(\.|({domain}[^\s]+))""",
"""\sduid=({login_id}[^\s]+)""",
"""dproc=(?: |({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+)))\s+\w+=""",
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "dest_ip->host", "dest_host->host","dest_user->account" ]


}
```