#### Parser Content
```Java
{
Name = "anywhere365-a-kv-app-activity-success-callreceive"
Conditions = [
  """ CallReceivedOnEndpoint: """
]
Vendor = "Anywhere365"
Product = "Anywhere365"
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
  """\s({event_id}\w+-\w+-\w+-\w+-\w+)\s"""
  """CallReceivedOnEndpoint:\s'sip:({dest_email_address}[^@]+[^\.]+\.[^,\s;']+)"""
]


}
```