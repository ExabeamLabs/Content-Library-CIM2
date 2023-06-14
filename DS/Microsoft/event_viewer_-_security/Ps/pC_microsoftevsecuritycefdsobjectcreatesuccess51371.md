#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-ds-object-create-success-5137-1
Vendor = Microsoft
Product = Event Viewer - Security
TimeFormat = "epoch"
Conditions = ["""A directory service object was created""", """|Microsoft-Windows-Security-Auditing:5137|"""]
Fields = [
  """({event_name}A directory service object was created)""",
  """({event_code}5137)""",
  """\srt=({time}\d{13})""",
  """categoryOutcome=\/?({result}[^=]+)\s\w+=""",
  """dhost=({dest_host}[\w\-.]+)""",
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  """duser=({user}[^=]+)\s\w+=""",
  """dntdom=({domain}[^\s\\]+)""",
  """suid=({user_sid}[^=]+)\s\w+=""",
  """categoryBehavior=([^=]+?\/|\/)?({action}[^=]+?)\s\w+=""",
  """cs6=({object_dn}.+?)\s\w+="""  ,
  """cs5=({object_class}[^=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```