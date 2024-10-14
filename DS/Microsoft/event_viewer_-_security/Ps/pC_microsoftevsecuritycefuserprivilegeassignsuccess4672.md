#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [ """CEF:""", """|Microsoft|Microsoft Windows|""", """externalId=4672""" ]
Fields = [
  """({event_name}Special privileges assigned to new logon)""",
  """\srt=({time}\d{13})""",
  """\sdeviceSeverity=({result}[^\s]+)""",
  """\sdhost=({host}[\w\-.]+?)(\s+\w+=|\s*$)""",
  """\sexternalId=({event_code}\d+)""",
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)""",
  """\sdntdom=({domain}.+?)(\s+\w+=|\s*$)""",
  """\sduid=({login_id}[^\s]+)""",
  """\sdpriv=({privileges}.+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```