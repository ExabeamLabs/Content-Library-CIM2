#### Parser Content
```Java
{
Name = rsa-ram-csv-app-notification-success-resourcecheck
  Conditions = [ """,Check Resource,Unprotected Resource,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}Check Resource)""",
    """({result}Unprotected Resource)"""
  ]
  ParserVersion = "v1.0.0"


}
```