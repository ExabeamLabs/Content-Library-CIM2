#### Parser Content
```Java
{
Name = rsa-ram-csv-app-authentication-success-validuser
  Conditions = [ """,User Token Created,Valid User,""" ]
  Fields = ${DLRSAParserTemplate.rsa-activity.Fields} [
    """({event_name}User Token Created),({action}Valid User),[^,]*\,(\s*|({additional_info}[^,]+)),"""
  ]
  ParserVersion = "v1.0.0"


}
```