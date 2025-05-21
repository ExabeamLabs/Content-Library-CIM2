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
    """Server IP\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Intruder IP\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"


}
```