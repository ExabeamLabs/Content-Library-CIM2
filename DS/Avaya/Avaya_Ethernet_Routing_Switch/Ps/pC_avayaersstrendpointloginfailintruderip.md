#### Parser Content
```Java
{
Name = avaya-ers-str-endpoint-login-fail-intruderip
  Vendor = Avaya
  Product = Avaya Ethernet Routing Switch
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Authentication Failure""", """Server IP""", """Intruder IP""" ]
  Fields = [
    """({event_name}Authentication Failure)""",
    """Server IP\s+({dest_ip}[a-fA-F\d.:]+)""",
    """Intruder IP\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]
  ParserVersion = "v1.0.0"


}
```