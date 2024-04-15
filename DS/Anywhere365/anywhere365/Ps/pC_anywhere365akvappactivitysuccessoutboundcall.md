#### Parser Content
```Java
{
Name = "anywhere365-a-kv-app-activity-success-outboundcall"
Conditions = [
  """ Outbound Call received from: """
]
Vendor = "Anywhere365"
Product = "Anywhere365"
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
  """\s({event_id}\w+-\w+-\w+-\w+-\w+)\s"""
  """Call received from:\s*sip:(({email_address}[^@]+@[^,\s;'']+)[,;\s]|({user}[^\s,]+))"""
  """to sip:({dest_email_address}[^@]+[^\.]+\.[^,\s;'']+)"""
]
DupFields = [
  "email_address->src_user"
  "user->src_user"
]


}
```