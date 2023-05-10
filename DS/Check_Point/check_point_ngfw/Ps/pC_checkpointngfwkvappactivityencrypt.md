#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-encrypt
  ParserVersion = "v1.0.0"
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "dMMMyyyy HH:mm:ss"
  Conditions = [ """|product=VPN-1 & FireWall-1""", """|i/f_name=""", """|action=encrypt""" ]
  Fields = [
    """\|time=\s*({time}\d+\w+\d\d\d\d \d\d:\d\d:\d\d)""",
    """\|orig=({host}[^\|]+)\|""",
    """\|service=({app_protocol}[^\|]+)\|""",
    """\|action=({action}[^\|]+)\|""",
    """\|rule_name=({rule}[^\|]+)\|""",
    """\|src=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\|]+))\|""",
    """\|s_port=({src_port}\d+)""",
    """\|dst=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\|]+))\|""",
    """\|proto=({protocol}[^\|]+)\|""",
    """\|xlatesport=({src_translated_port}\d+)""",
    """\|xlatedport=({dest_translated_port}\d+)"""
  ]


}
```