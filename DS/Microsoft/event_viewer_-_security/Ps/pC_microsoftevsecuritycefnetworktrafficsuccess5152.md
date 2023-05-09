#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-network-traffic-success-5152
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:5152"""]
Fields = [
  """({event_name}The Windows Filtering Platform blocked a packet)""",
  """({event_code}5152)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """spt=({src_port}\d{1,5})""",
  """dpt=({dest_port}\d+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
]
ParserVersion = "v1.0.0"


}
```