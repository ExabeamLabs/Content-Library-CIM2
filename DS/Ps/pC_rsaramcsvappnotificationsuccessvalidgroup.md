#### Parser Content
```Java
{
Name = rsa-ram-csv-app-notification-success-validgroup
  Conditions = [ """,Returned Groups For User,Valid Group,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}Returned Groups For User)""",
    """({action}Valid Group)"""
  ]
  ParserVersion = "v1.0.0"


}
```