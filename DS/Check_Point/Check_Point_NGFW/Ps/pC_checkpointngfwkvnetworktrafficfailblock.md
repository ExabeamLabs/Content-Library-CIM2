#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-fail-block
  ParserVersion = v1.0.0  
  Conditions = [ """product=VPN-1 & FireWall-1""", """|i/f_name=""", """|action=block""" ]

s-checkpoint-firewall = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|orig=({host}[^\|]+)\|""",
    """\|i\/f_dir=({direction}[^\|]+)""",
    """\|service=({app_protocol}[^\|]+)\|""",
    """\|action=({action}[^\|]+)\|""",
    """\|app_rule_name=({rule}[^\|]+)\|""",
    """\|src=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\|]+))\|""",
    """\|s_port=({src_port}\d+)""",
    """\|dst=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\|]+))\|""",
    """\|proto=({protocol}[^\|]+)\|""",
    """\|src_machine_name=({src_host}[^\|]+)""",
    """\|src_user_name=[^(]+\(({user}[^)]+)""",
    """\|user=[^(]+\(({user}[^)]+)"""
  
}
```