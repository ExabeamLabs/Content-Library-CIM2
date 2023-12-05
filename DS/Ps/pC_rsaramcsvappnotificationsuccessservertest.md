#### Parser Content
```Java
{
Name = rsa-ram-csv-app-notification-success-servertest
  Conditions = [ """,Server Test,Server Test Succeeded,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}Server Test)""",
    """({result}Succeeded)"""
  ]
  ParserVersion = "v1.0.0"


}
```