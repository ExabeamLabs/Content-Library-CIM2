#### Parser Content
```Java
{
Name = rsa-netwitness-cef-app-logout-success-audit
  Conditions = [ """CEF:""", """RSA|NetWitness Audit""", """AUTHENTICATION|logoff""", """outcome=success""" ]
  Fields = ${DLRSAParserTemplate.cef-rsa-system-event.Fields}[
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d\d:\d\d)\s*({host}[^\s]+)""",
    """\ssourceServiceName =({app}.+?)\s*\w+=""",
    """\sdeviceExternalId=({external_id}.+?)\s*\w+=""",
    """\sdeviceProcessName =({process_name}.+?)\s*\w+=""",
    """\scs2=(null|({group_name}.+?))\s*\w+=""",
    """\sactionType=(null|({action_type}.+?))\s*\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```