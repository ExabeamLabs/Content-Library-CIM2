#### Parser Content
```Java
{
Name = "infoblox-bddi-str-endpoint-login-success-dhcpack"
  ParserVersion = "v1.0.0"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss", "MMM  dd HH:mm:ss", "MMM d HH:mm:ss", "MMM  d HH:mm:ss"]
  Conditions = [
""" dhcpd[""",
""": DHCPACK """
  ]
  Fields = [
"""({host}\S+) dhcpd\[""",
"""({event_name}DHCPACK)"""
""": DHCPACK to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? \(({dest_mac}[^\s\)]+)\)""",
""": DHCPACK on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? to ({dest_mac}[^\s]+) (\(({dest_host}[\w\-.]+)\))?"""
"""\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*dhcpd\[""",
"""({time}\w+\s+\d+\s+\d+:\d+:\d+)\s""",
"""lease-duration\s+({ip_lease_time}\d+)"""
"""uid\s+({user_id}[^\n\s"]+)"""
  ]


}
```