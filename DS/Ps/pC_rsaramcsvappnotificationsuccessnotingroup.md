#### Parser Content
```Java
{
Name = rsa-ram-csv-app-notification-success-notingroup
  Conditions = [ """,User Not In Group,User Not In Group,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}User Not In Group)""",
    """({result}User Not In Group)"""
  ]
  ParserVersion = "v1.0.0"


}
```