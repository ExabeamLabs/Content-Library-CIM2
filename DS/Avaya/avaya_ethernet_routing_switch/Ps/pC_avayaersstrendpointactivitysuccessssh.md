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
      """ssh\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\)""",
      """days,\s*[\d:]*\s*({process_command_line}[^$"]+?)(\s*$|\s*")"""
  ]


}
```