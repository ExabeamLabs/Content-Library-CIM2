#### Parser Content
```Java
{
Name = "cisco-asa-str-network-traffic-success-teardown-2"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco" 
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
"""%ASA-"""
"""-30201"""
""": Teardown """
""" duration """
  ]
  Fields = [
"""({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)"""
"""(\w{3} (\d\d| \d) \d\d\d\d (\d\d| \d):\d\d:\d\d)\s+(::ffff:)?({host}[\w\.-]+)\s*:\s*%ASA-"""
"""%ASA-({priority}\d+)-({event_code}\d+)"""
"""({event_name}Teardown ({protocol}\w+) connection)"""
"""\sconnection\s+({connection_id}\d+)"""
"""\sfor\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\/({src_port}\d+)"""
"""\sto\s+({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))\/({dest_port}\d+)"""
"""\sduration\s+({duration}\S+)\s+bytes\s+({bytes}\d+)(\s+({reason}[^\("]+[^\(\s"])\s)?(\((({email_address}[^@\)]+@[^\)]+)|({user}[^\)]+))\))?"""
"""%ASA-.*?\((({domain}[^\\\/]+)[\\\/]+)?(({email_address}[^@\)]+@[^\)]+)|({user}[^\\\/]+?))\)"""
  ]
  DupFields = [
"event_name->operation"
  ]


}
```