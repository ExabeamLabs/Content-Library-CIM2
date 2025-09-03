#### Parser Content
```Java
{
Name = "cisco-fp-kv-network-traffic-success-430002"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
    """AccessControlRuleAction: """
    """IngressInterface: """
    """EventPriority:"""
    """%FTD"""
	"""-430002"""
  ]
  Fields = [
    """({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*"""
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """SrcPort:\s*({src_port}\d+)"""
    """DstPort:\s*({dest_port}\d+)"""
    """AccessControlRuleAction:\s*({result}[^,]+)"""
    """Protocol:\s*({protocol}[^,]+)"""
    """IngressInterface:\s*({src_interface}[^,]+)"""
    """EgressInterface:\s*({dest_interface}[^,]+)"""
    """ACPolicy:\s*({policy_name}[^,]+)"""
    """InitiatorPackets:\s*({packets_in}\d+)"""
    """ResponderPackets:\s*({packets_out}\d+)"""
    """InitiatorBytes:\s*({bytes_in}\d+)"""
    """ResponderBytes:\s*({bytes_out}\d+)"""
    """DeviceUUID: ({device_id}[^\s]+)"""
    """\WIngressZone:\s*({ingress_zone}[^,]+)"""
    """EgressZone:\s*({egress_zone}[^,]+)"""
  ]
  DupFields = [ "result->action" ]


}
```