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
    """Authentication ({result}[^\s]+) for SNMP req from host (({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)) TAG: Network"""
  
]


}
```