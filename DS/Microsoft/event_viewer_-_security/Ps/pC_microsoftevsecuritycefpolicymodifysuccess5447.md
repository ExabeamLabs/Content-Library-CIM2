#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-policy-modify-success-5447
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:5447"""]
Fields = [
  """({event_name}A Windows Filtering Platform filter has been changed)""",
  """({event_code}5447)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """duser=({user}[^=]+)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """ad\.ChangeType=({change_type}[^=]+)\s[\w.]+=""",
  """ad\.FilterName =({filter_name}[^=]+)\s[\w.]+="""
]
ParserVersion = "v1.0.0"


}
```