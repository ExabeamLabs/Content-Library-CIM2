#### Parser Content
```Java
{
Name = cisco-fp-str-network-traffic-fail-106016
  Vendor = "Cisco" 
  Product = "Cisco Firepower"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-106016""", """ Deny IP spoof from """, """ on interface """ ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)\s""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",    
    """({event_name}({operation}({action}Deny) IP spoof)\sfrom\s\(?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?\)?\sto\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))? on interface\s({interface}[^\s"]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```