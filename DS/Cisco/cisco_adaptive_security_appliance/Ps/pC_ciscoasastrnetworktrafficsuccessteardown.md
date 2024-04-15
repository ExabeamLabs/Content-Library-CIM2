#### Parser Content
```Java
{
Name = "cisco-asa-str-network-traffic-success-teardown"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
"""%ASA-"""
"""-30202"""
"""Teardown """
""" connection """
  ]
  Fields = [
"""({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)"""
"""(\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)\s+(::ffff:)?({host}[\w\.-]+)\s*:\s*%ASA-"""
"""%ASA-({priority}\d+)-({event_code}\d+)"""
"""({event_name}Teardown ({protocol}\w+) connection)"""
"""\sfaddr\s+(((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))((\/({dest_port}\d+))|(\s|$))|({icmp_seq_num}\S+))"""
"""\sgaddr\s+(((::ffff:)?({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_translated_host}[^\s]+?))((\/({dest_translated_port}\d+))|(\s|$))|({icmp_type}\S+))"""
"""\sladdr\s+((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))((\/({src_port}\d+))|(\s|$))"""
"""for\s+[^\s:]+:\s*(((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))((\/({src_port}\d+))|(\s|$))|({icmp_type}\S+))"""
"""to\s+[^\s:]+:\s*((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))((\/({dest_port}\d+))|(\s|$))"""
"""\sbytes\s+({bytes}\d+)"""
"""%ASA-.*?\((({domain}[^\\/]+)[\\/]+)?(?:({email_address}[^@\\/]+@[^@\\/]+?)|({user}[^\\/]+?))\)"""
  ]
  DupFields = [
"event_name->operation"
  ]


}
```