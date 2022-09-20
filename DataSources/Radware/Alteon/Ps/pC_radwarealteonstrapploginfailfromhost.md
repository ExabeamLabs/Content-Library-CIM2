#### Parser Content
```Java
{
Name = radware-alteon-str-app-login-fail-fromhost
  Vendor = Radware
  Product = Alteon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """: Failed login attempt """, """from host""", """>: """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+({alert_type}\S+)\s+({app}\S+)\s+""",
    """({operation}({result}Failed) login attempt) via ({resource}.+?) from host (({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}\S+))""",
  ]


}
```