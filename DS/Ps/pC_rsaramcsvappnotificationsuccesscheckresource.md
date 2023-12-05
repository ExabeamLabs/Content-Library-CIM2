#### Parser Content
```Java
{
Name = rsa-ram-csv-app-notification-success-checkresource
  Conditions = [ """,Check Resource,Protected Resource,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}Check Resource)""",
    """({result}Protected Resource)"""
  ]
  ParserVersion = "v1.0.0"


}
```