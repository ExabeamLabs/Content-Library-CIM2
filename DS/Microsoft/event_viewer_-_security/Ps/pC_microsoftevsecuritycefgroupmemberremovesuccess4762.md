#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-group-member-remove-success-4762
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""A member was removed from a security-disabled universal group""", """|Microsoft-Windows-Security-Auditing:4762|"""]
Fields = [
  """({event_name}A member was removed from a security-disabled universal group)""",
  """({event_code}4762)""",
  """\srt=({time}\d{13})""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
  """dntdom=({domain}[^\s\\]+)""",
  """suid=({user_sid}[^=]+)\s\w+=""",
  """categoryBehavior=([^=]+?\/|\/)?({action}[^=]+?)\s\w+=""",
  """cs6=(({group_domain}[^\\=]+)\\+)?({group_name}[^=]+?)\s\w+="""  
]
ParserVersion = "v1.0.0"


}
```