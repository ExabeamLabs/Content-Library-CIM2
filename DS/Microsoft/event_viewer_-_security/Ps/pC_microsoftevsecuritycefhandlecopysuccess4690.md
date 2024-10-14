#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-handle-copy-success-4690
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4690"""]
Fields = [
  """({event_name}An attempt was made to duplicate a handle to an object)""",
  """({event_code}4690)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """aid=({aid}[^\s\\]+)""",
  """cs3=({process_id}[^=]+)\s\w+=""",
]
ParserVersion = "v1.0.0"


}
```