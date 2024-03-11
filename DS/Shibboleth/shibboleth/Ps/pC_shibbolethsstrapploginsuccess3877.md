#### Parser Content
```Java
{
Name = shibboleth-s-str-app-login-success-3877
  Vendor = Shibboleth
  Product = Shibboleth
  TimeFormat = "yyyyMMdd'T'HHmmss"
  Conditions = [ """<cont-3877_conditions>""" ]
  Fields = [
    """({time}\d{8}T\d{6}Z)\|""",
    """([^\|]*\|){3}({app}[^\|]+)\|""",
    """([^\|]*\|){8}({user}[^\|]+)\|""",
  ]
  ParserVersion = v1.0.0


}
```