#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-password-reset-success-4724"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """externalId=4724 """
  """An attempt was made to reset an account's password."""
]
Fields = [
  """\sdhost=({host}[\w\-.]+)"""
  """({event_name}An attempt was made to reset an account's password)"""
  """Microsoft-Windows-Security-Auditing:({event_code}\d{4})"""
  """\srt=({time}\d{13})"""
  """\ssntdom=({domain}[^\s]+)"""
  """\ssuser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """\sduser=({dest_user}.+?)\s+\w+="""
  """\ssuid=({logon_sid}[^\s]+)"""
  """Security_,ID=({user_sid}[^\s]+?)(\s|\||$)"""
  """\sdntdom=({dest_domain}.+?)\s+\w+="""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```