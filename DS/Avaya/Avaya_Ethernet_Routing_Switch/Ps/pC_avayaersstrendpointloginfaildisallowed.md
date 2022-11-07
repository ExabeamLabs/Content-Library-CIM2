#### Parser Content
```Java
{
Name = avaya-ers-str-endpoint-login-fail-disallowed
    Vendor = Avaya
    Product = Avaya Ethernet Routing Switch
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Disallowed connection""", """ :#1""", """IP address:""" ]
    Fields = [
      """({event_name}Disallowed connection)""",
      """IP address:\s+({src_ip}[a-fA-F\d.:]+)""",
  ]


}
```