#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-computername"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Special privileges assigned to new logon"""
  """Privileges"""
  """"computer_name"""
]
Fields = [
  """({event_name}Special privileges assigned to new logon)"""
  """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)"""
  """\"(?:winlog\.)?computer_name\\*\":\\*\"({src_host}({host}[\w\-.]+))"""
  """@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """Type\s*=\s*\"({result}[^\";]+)\""""
  """Keywords=({result}.+?);?\s*(\w+=)"""
  """<Computer>({src_host}({host}[\w\-.]+))</Computer>"""
  """Computer(\w+)?[\"\s]*(:|=)\s*\"?({src_host}({host}[\w\-.]+))"""
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """({event_code}4672)"""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
  """Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)"""
  """\s*Logon ID(:|=)\s*({login_id}.+?)[\s;]*Privileges(:|=)\s*({privileges}.+?)(<|\s*User:|\s+\d+|,|\s*\"|;|\s*$)"""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
  """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?""""
  """PrivilegeList\\?\"+:\\?\"({privileges}[^\"]+?)\\?\""""
  """SubjectDomainName\\?\"+:\\?\"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?\""""
]
ParserVersion = "v1.0.0"


}
```