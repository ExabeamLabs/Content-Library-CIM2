#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-assign-success-4673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [ """CEF:""", """|Microsoft|Microsoft Windows|""", """|A privileged service was called""" ]
Fields = [
  """({event_name}A privileged service was called)"""
  """\srt=({time}\d{13})""",
  """\sdeviceSeverity=({result}[^\s]+)""",
  """\sdhost=({dest_host}({host}[\w\-.]+?))(\s+[^\s]+=|\s*$)""",
  """\sexternalId=({event_code}\d+)""",
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[^\s]+=|\s*$)""",
  """\sdntdom=({domain}.+?)(\s+[^\s]+=|\s*$)""",
  """\sad.Service:Server=({object_server}.+?)(\s+[^\s]+=|\s*$)""",
  """\sduid=({login_id}[^\s]+)""",
  """:Privileges=({privileges}.+?)(\s+[^\s]+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```