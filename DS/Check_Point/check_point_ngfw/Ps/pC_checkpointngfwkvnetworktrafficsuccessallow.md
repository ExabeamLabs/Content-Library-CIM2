#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-network-traffic-success-allow"
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""product=VPN-1 & FireWall-1""", """|i/f_name=""", """|action=allow"""]
  Fields = [
"""\"time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\|orig=({host}[^\|]+)\|"""
"""\|i\/f_dir=({direction}[^\|]+)"""
"""\|service=({app_protocol}[^\|]+)\|"""
"""\|action=({action}[^\|]+)\|"""
"""\|app_rule_name=({rule}[^\|]+)\|"""
"""\|src=(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\|]+))\|"""
"""\|s_port=({src_port}\d+)"""
"""\|dst=(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\|]+))\|"""
"""\|proto=({protocol}[^\|]+)\|"""
"""\|src_machine_name=({src_host}[^\|]+)"""
"""\|src_user_name=[^(]+\(({user}[^)]+)"""
"""\|user=[^(]+\(({user}[^)]+)"""
  ]


}
```