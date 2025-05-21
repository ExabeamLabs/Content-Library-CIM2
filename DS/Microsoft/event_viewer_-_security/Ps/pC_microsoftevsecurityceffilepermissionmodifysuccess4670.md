#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-file-permission-modify-success-4670
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4670"""]
Fields = [
  """({event_name}Permissions on an object were changed)""",
  """({event_code}4670)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """cs3=({process_id}[^=]+)\s\w+=""",
  """fileType=({object_type}[^=]+)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```