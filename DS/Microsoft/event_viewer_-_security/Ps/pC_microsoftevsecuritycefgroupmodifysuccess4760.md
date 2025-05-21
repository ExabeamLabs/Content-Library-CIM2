#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-group-modify-success-4760
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""A security-disabled universal group was changed""", """|Microsoft-Windows-Security-Auditing:4760|"""]
Fields = [
  """({event_name}A security-disabled universal group was changed)""",
  """({event_code}4760)""",
  """\srt=({time}\d{13})""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
  """sntdom=({domain}[^\s\\]+)""",
  """suid=({user_sid}[^=]+)\s\w+=""",
  """categoryBehavior=([^=]+?\/|\/)?({action}[^=]+?)\s\w+=""" ,
  """duser=({dest_user}[^=]+?)\s\w+="""  
]
ParserVersion = "v1.0.0"


}
```