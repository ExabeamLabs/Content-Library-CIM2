#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-group-member-list-success-4799
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""|Microsoft|Microsoft Windows|""", """Microsoft-Windows-Security-Auditing:4799"""]
Fields = [
  """({event_name}A security-enabled local group membership was enumerated)""",
  """({event_code}4799)""",
  """\srt=({time}\d{13})""",
  """\sdvchost=({host}[^\s]+)""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """msg=({additional_info}[^=]+)\s\w+=""",
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
  """dntdom=({domain}[^\s]+)""",
  """filePath=({object}[^=]+)\s\w+=""",
  """fileType=({object_type}[^=]+)\s\w+=""",
  """suid=({user_sid}[^=]+)\s\w+="""	
]
ParserVersion = "v1.0.0"


}
```