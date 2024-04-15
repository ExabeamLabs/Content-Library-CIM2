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
  """computer_name"""
]
Fields = [
  """({event_name}Special privileges assigned to new logon)"""
  """\scategoryOutcome=(|/({action}.+?))(\s+\w+=|\s*$)"""
  """\"(?:winlog\.)?computer_name\\*\":\\*\"({host}[^\\\"]+)"""
  """@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """Type\s*=\s*\"({action}[^\";]+)\""""
  """Keywords=({action}.+?);?\s*(\w+=)"""
  """<Computer>({host}[^<]+)</Computer>"""
  """Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}[^\s\";]+)"""
  """({event_code}4672)"""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^\\]+))\\?"""",
  """Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)"""
  """\s*Logon ID(:|=)\s*({login_id}.+?)[\s;]*Privileges(:|=)\s*({privileges}.+?)(<|\s*User:|\s+\d+|,|\s*\"|;|\s*$)"""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?""""
  """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?""""
  """PrivilegeList\\?\"+:\\?\"({privileges}[^\"]+?)\\?\""""
  """SubjectDomainName\\?\"+:\\?\"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?\""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```