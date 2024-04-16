#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-sequencenum
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """"product=VPN-1 & FireWall-1""", """SmartDefense""", """CheckPoint""", """sequencenum""" ]
  Fields = [
    """\Wtime:"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """ifdir:"+({direction}[^"]+)""",
    """originsicname:"+({user_ou}[^"]+)"""
    """\Wproduct:"({product_name}[^"]+)""",
    """sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```