#### Parser Content
```Java
{
Name = rsa-ram-csv-app-authentication-success-request
  Conditions = [ """,Request To AdaptiveAuth Store,Succeeded,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}Request To AdaptiveAuth Store)""",
    """({result}Succeeded)"""
  ]
  ParserVersion = "v1.0.0"


}
```