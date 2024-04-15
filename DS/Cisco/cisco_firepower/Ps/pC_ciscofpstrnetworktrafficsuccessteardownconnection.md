#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-teardown-connection"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """%FTD-"""
    """-30202"""
    """Teardown """
    """ connection """
  ]
  Fields = [
    """({host}[\w\-.]+)\s*:\s*%FTD-"""
    """\s*({host}[^\s]+)\s\w{1,3}\s\d{1,2}\s\d\d:\d\d:\d\d\s""",
    """%FTD-({priority}\d+)-({event_code}\d+)"""
    """({event_name}Teardown ({protocol}\w+) connection)"""
    """\sfaddr\s+((({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+))|(\s|$))|({icmp_seq_num}\S+))"""
    """\sgaddr\s+((({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_translated_host}[^\s]+?))((\/({dest_translated_port}\d+))|(\s|$))|({icmp_type}\S+))"""
    """\sladdr\s+(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+))|(\s|$))"""
    """for\s+[^\s:]+:\s*((({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+))|(\s|$))|({icmp_type}\S+))"""
    """to\s+[^\s:]+:\s*(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+))|(\s|$))"""
    """\sbytes\s+({bytes}\d+)"""
    """%FTD-.*?\((({domain}[^\\\/]+)[\\\/]+)?(?:({email_address}[^@\\\/]+@[^@\\\/]+?)|({user}[^\\\/]+?))\)"""
  ]
  DupFields = [
    "event_name->operation"
  ]


}
```