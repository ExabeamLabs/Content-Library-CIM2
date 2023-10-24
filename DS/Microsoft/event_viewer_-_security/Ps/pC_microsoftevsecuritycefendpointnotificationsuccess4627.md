#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-notification-success-4627
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4627"""]
Fields = [
  """({event_name}Group membership information)""",
  """({event_code}4627)""",
  """\srt=({time}\d{13})""",
  """\sdntdom=({domain}[^\s]+)""",
  """\sduser=({user}[\w\.\-]{1,40}\$?)\s+\w+=""",
  """\sduid=({login_id}[^\s]+)""",
  """\scn1=({login_type}\d+)""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """cs1=({group_membership}[^=]+)\s\w+="""
]
DupFields = ["host->dest_host"]
ParserVersion = "v1.0.0"


}
```