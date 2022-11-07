#### Parser Content
```Java
{
Name = avaya-ers-str-endpoint-logout-success-sessionclosed
    Vendor = Avaya
    Product = Avaya Ethernet Routing Switch
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Session closed""", """ :#6""", """IP address:""" ]
    Fields = [
      """({event_name}Session closed)""",
      """IP address:\s+({src_ip}[a-fA-F\d.:]+)""",
  ]


}
```