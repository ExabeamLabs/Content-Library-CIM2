#### Parser Content
```Java
{
Name = avaya-ers-str-endpoint-login-fail-unauthorized
    Vendor = Avaya
    Product = Avaya Ethernet Routing Switch
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """:Unauthorized connection""", """IP address:""" ]
    Fields = [
      """({event_name}Unauthorized connection)""",
      """IP address:\s+({src_ip}[a-fA-F\d.:]+)""",
  ]


}
```