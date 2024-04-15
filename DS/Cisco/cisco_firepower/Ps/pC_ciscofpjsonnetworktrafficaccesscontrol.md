#### Parser Content
```Java
{
Name = "cisco-fp-json-network-traffic-accesscontrol"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """"protocol":"""
    """"recordType": 71,"""
    """"eventType":"""
    """"recordTypeDescription":"""
  ]
  Fields = [
    """\"eventDateTime\": \"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\"sensor\": \"({host}[^\"]+)\""""
    """\"firewallRuleAction\": \"({action}[^\"]+)\""""
    """\"firewallRule\": \"({rule}[^\"]+)\""""
    """\"initiatorIpAddress\": \"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\"responderIpAddress\": \"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\"responderPort\": ({dest_port}\d+)"""
    """\"clientApplication\": \"(Unknown|({network_app}[^\"]+))\""""
    """\"transportProtocol\": \"({protocol}[^\"]+)\""""
    """\"initiatorTransmittedBytes\": ({bytes_out}\d+)"""
    """\"responderTransmittedPackets\": ({bytes_in}\d+)"""
    """\"ingressInterface\": \"({src_interface}[^\"]+)\""""
    """\"egressInterface\": \"({dest_interface}[^\"]+)\""""
    """\"user\": \"(No Authentication Required|(?i)Unknown|({user}[^\"]+))\""""
    """\"recordTypeDescription\": \"({event_name}[^\"]+)\""""
    """\"clientUrl\":[^\]]+?\"data\": \"({additional_info}[^\"]+)\""""
    """\"initiatorPort\": ({src_port}\d+)"""
  ]


}
```