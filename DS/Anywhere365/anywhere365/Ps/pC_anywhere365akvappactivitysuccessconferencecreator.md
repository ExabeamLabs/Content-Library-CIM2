#### Parser Content
```Java
{
Name = "anywhere365-a-kv-app-activity-success-conferencecreator"
Conditions = [
  """UccConferenceCreator id"""
]
Vendor = "Anywhere365"
Product = "Anywhere365"
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
  """\s({event_id}\w+-\w+-\w+-\w+-\w+)\s"""
  """id\s*:'*({alert_id}\w+)"""
]


}
```