#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-775002
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-775002""" ]
  Fields = [
    """({host}[\w\-.]+)\s+({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """from\s+({src_interface}[^:]+):\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))\/({src_port}\d+)\s*\((({domain}[^\\]+)\\+)?({src_host}[\w\-.]+)""",
"""to\s+({dest_interface}[^:]+):\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)""",
    """({event_name}Duplicate Mapped Source Socket)""",
    """-775002:\s*([^:]+):\s*({result_reason}.+?)\s*(((\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|([^\s]+?))\/(\d+)\s*\-\s*({protocol}\S+)"""
	# DL Fields are removed
  ]


}
```