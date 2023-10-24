#### Parser Content
```Java
{
Name = "cisco-umbrella-cef-network-traffic-success-ip"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Umbrella"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""destinationServiceName =Cisco Umbrella """
"""dproc=IP """
""""identity":""""
  ]
  Fields = [

"""({app}Cisco Umbrella)"""
"""\"timestamp\"+:\"+({time}[^\",]+)\""""
"""\"categories\"+:\[\"+({category}[^\",]+)"""
"""\"sourceIp\"+:\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""\"sourcePort\"+:\"+({src_port}\d+)\""""
"""\"destinationIp\"+:\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\"destinationPort\"+:\"+({dest_port}\d+)"""
"""\"identity\"+:\"+({dest_host}[^\"]+)\""""
  ]


}
```