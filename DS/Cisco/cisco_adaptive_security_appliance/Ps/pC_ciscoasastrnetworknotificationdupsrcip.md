#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-dupsrcip
  ParserVersion = v1.0.0
  Conditions = [ """%ARP-2-DUP_SRC_IP:""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields}[
    """packet received from\s+({src_mac}[^\s]+?)\s+on""",
    """duplicate of local,\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```