#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-logout-success-4634
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4634"""]
Fields = [
  """({event_name}An account was logged off)""",
  """({event_code}4634)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """cn1=({login_type}\d+)""",
  """duser=({user}[^=]+)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """aid=({aid}[^\s\\]+)"""
]
ParserVersion = "v1.0.0"


}
```