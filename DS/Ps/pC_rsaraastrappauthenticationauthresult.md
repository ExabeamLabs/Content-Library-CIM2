#### Parser Content
```Java
{
Name = rsa-raa-str-app-authentication-authresult
  ParserVersion = v1.0.0
  Conditions = [ """AAOP-Audit""", """AUTH_RESULT""" ]
  Fields = ${DLRSAParserTemplate.rsa-account-activity.Fields} [
    """AUTH_RESULT_RESULT=({result}\w+)""",
  ]


}
```