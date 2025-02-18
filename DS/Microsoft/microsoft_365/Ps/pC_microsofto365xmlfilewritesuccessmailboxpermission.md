#### Parser Content
```Java
{
Name = "microsoft-o365-xml-file-write-success-mailboxpermission"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """succeeded"""
  """><Channel>"""
  """MailboxPermission"""
]
Fields = [
  """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>({host}[^\s\<]+)"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """><Message>Cmdlet ({result}[^"\\\.]+)"""
  """<Channel>({app}.+?)<\/Channel>"""
  """AccessRights=\{({additional_info}.+?)\}\}</Data><Data>.+?({full_name}[^\\\/]+?)<\/Data>"""
  """, User=({object}[^,]+)"""
  """<Data>\{Identity=({resource}[^,]+)"""
  """<EventData><Data>({operation}.+?)<\/Data>"""
  """User=(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```