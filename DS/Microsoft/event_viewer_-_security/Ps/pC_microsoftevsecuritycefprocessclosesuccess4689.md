#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-process-close-success-4689
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4689"""]
Fields = [
  """({event_name}A process has exited)""",
  """({event_code}4689)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dproc=({process_path}({process_dir}[^=]+)\\({process_name}[^=]+))\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """msg=({additional_info}[^=]+)\s\w+=""",
  """duser=({user}[^=]+)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """cs3=({process_id}[^=]+)\s\w+=""",
]
ParserVersion = "v1.0.0"


}
```