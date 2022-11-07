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
    """\Wtime:"({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """ifdir:"+({direction}[^"]+)""",
    """originsicname:"+({user_ou}[^"]+)"""
    """\Wproduct:"({product_name}[^"]+)""",
    """sourceip="({src_ip}[^"]+)"""
  ]


}
```