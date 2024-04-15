#### Parser Content
```Java
{
Name = "cisco-fp-kv-network-traffic-success-accesscontrol"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
    """AccessControlRuleAction: """
    """IngressInterface: """
    """AccessControlRuleName: """
    """InitiatorPackets: """
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[\w\-.]+)?\s*(\(|\%)"""
    """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """SrcPort:\s*({src_port}\d+)"""
    """DstPort:\s*({dest_port}\d+)"""
    """AccessControlRuleAction:\s*({action}[^,]+)"""
    """Protocol:\s*({protocol}[^,]+)"""
    """IngressInterface:\s*({src_interface}[^,]+)"""
    """EgressInterface:\s*({dest_interface}[^,]+)"""
    """ACPolicy:\s*({policy_name}[^,]+)"""
    """AccessControlRuleName:\s*({rule}[^,]+)"""
    """User:\s*(Unknown|No Authentication Required|({user}[^,\s]+))"""
    """ConnectionDuration:\s*({connection_duration}[^,]+)"""
    """InitiatorPackets:\s*({packets_in}\d+)"""
    """ResponderPackets:\s*({packets_out}\d+)"""
    """InitiatorBytes:\s*({bytes_in}\d+)"""
    """ResponderBytes:\s*({bytes_out}\d+)"""
    """URL:\s+({url}[^,\s"]+)""",
    """URL:\s+(?:-|\w+:\/+)({web_domain}[^\s\/:]+)""",
    """URL:\s+(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)"""
  ]


}
```