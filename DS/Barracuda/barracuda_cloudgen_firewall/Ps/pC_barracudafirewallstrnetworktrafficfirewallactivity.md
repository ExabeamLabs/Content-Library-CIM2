#### Parser Content
```Java
{
Name = "barracuda-firewall-str-network-traffic-firewallactivity"
Vendor = "Barracuda"
Product = "Barracuda Cloudgen Firewall"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """/box_Firewall_Activity: """
]
Fields = [
  """\/box_Firewall_Activity:\s+[^\s]+\s+({host}[^\s]+)\s+({operation}[^\s:]+):\s+""",
  """\/box_Firewall_Activity:\s+-([\d:\d]+\s\w+)?\s*({host}[^\s]+)\s+({operation}[^\s:]+):\s+"""
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}({event_code}[^\|\s]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}[^\|]*\|({protocol}[^\|]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){2}({src_interface}[^\|]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){3}(?:0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){4}({src_port}\d+)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){5}({src_mac}[^\|]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){6}(?:0.0.0.0|({dest_external_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){7}({dest_port}\d+)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){8}({app_protocol}[^\|]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){9}({dest_interface}[^\|]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){10}({rule}[^\|]+)\|""",
  """\s+(Allow|Remove|LocalRemove|LocalAllow):\s+([^\|]*\|){11}({action}[^\|]+)\|""",
  """\s+(Drop|Block|LocalBlock):\s+([^\|]*\|){11}({failure_reason}[^\|]+)\|""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){12}(?:0.0.0.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){13}(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){14}({duration}\d+)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){16}({bytes_in}\d+)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){17}({bytes_out}\d+)""",
  """\/box_Firewall_Activity:\s+([^\s]+\s+){3}([^\|]*\|){20}(-|({email_address}[^@"\s]+@[^@"\s\|]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-]{1,40}\$?)))\|"""
]
ParserVersion = "v1.0.0"


}
```