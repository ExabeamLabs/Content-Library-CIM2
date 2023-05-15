#### Parser Content
```Java
{
Name = cisco-asa-str-app-activity-success-network
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """TAG: Network""" ]
  Fields = [
    """Authentication ({result}[^\s]+) for SNMP req from host (({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)) TAG: Network"""
  
]


}
```