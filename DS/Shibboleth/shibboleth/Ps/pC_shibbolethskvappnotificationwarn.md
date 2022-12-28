#### Parser Content
```Java
{
Name = shibboleth-s-kv-app-notification-warn
  Product = Shibboleth
  Vendor = Shibboleth
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """shibboleth: WARN""" ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+shibboleth:""",
    """({app}Shibboleth)""",
    """Shibboleth\.Application\s*:\s*({event_name}.+?)\s*$""",
  ]


}
```