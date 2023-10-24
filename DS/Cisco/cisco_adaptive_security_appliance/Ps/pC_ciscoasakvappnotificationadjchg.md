#### Parser Content
```Java
{
Name = cisco-asa-kv-app-notification-adjchg
  ParserVersion = "v1.0.0"
  Conditions = [ """%OSPF-""", """ADJCHG:""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """ADJCHG:\s*.+?({event_name}Nbr ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?[^,]+)""",
    """Neighbor Down:\s*({result_reason}.+?)\s+$""",
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec"]
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```