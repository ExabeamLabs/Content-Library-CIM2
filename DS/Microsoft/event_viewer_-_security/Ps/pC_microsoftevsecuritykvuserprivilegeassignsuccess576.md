#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-assign-success-576"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """EventCode=576"""
  """Special privileges assigned to new logon"""
]
Fields = [
  """({event_name}Special privileges assigned to new logon)"""
  """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
  """\sEventCode=({event_code}\d+)"""
  """\sType=({action}.+?)(\s+\w+=|\s*$)"""
  """\sComputerName =({host}.+?)(\s+\w+=|\s*$)"""
  """\sUser=({user}.+?)(\s+\w+=|\s*$)"""
  """\sSid=({user_sid}.+?)(\s+\w+=|\s*$)"""
  """\s*Domain:\s*(?:-|({domain}.*?))\s*Logon ID:\s*\(?({login_id}[^)]*)\)?\s*Privileges:\s*({privileges}.*?)\s*$"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```