#### Parser Content
```Java
{
Name = avaya-ers-str-endpoint-activity-success-ssh
    Vendor = Avaya
    Product = Avaya Ethernet Routing Switch
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ :S """, """ssh(""", """days,""" ]
    Fields = [
      """ssh\(({src_ip}[a-fA-F\d.:]+):({src_port}\d+)\)""",
      """days,\s*[\d:]*\s*({process_command_line}[^$"]+?)(\s*$|\s*")"""
  ]


}
```