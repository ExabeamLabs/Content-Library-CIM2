#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-handle-request-success-4656-1
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4656"""]
Fields = [
  """({event_name}A handle to an object was requested)""",
  """({event_code}4656)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """aid=({aid}[^\s\\]+)""",
  """cs3=({process_id}[^=]+)\s\w+=""",
  """dproc=({process_path}({process_dir}[^=]+)\\({process_name}[^=]+))\s\w+=""",
  """fname=({object}[^=]+)\s\w+=""",
  """fileType=({object_type}[^=]+)\s\w+=""",
  """cs1=({privileges}[^=]+)\s\w+=""",
]
ParserVersion = "v1.0.0"


}
```