#### Parser Content
```Java
{
Name = cisco-fp-kv-network-traffic-success-permitany
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%FTD-""", """Permit Any""" ]
  Fields = [
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)\\?""",
    """({event_name}Permit Any)""",
    """AccessControlRuleAction="+({result}[^"]+)"+""",
    """SrcIP="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+""",
    """DstIP="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+""",
    """SrcPort="+({src_port}\d+)"+""",
    """DstPort="+({dest_port}\d+)"+""",
    """\sProtocol="+({protocol}[^"]+)"+""",
    """IngressInterface="+({ingress_interface}[^"]+)"+""",
    """EgressInterface="+({egress_interface}[^"]+)"+""",
    """DeviceUUID="+({device_id}[^"]+)"+""",
    """Client="+({app}[^"]+)"+""",
    """ApplicationProtocol="+({app_protocol}[^"]+)"+""",
    """InitiatorBytes="+({bytes_in}\d+)"+""",
    """ResponderBytes="+({bytes_out}\d+)"+""",
    """NAPPolicy="+({nap_policy}[^"]+)"+""",
    """URL="+({url}[^"]+)"+""",
    """InitiatorPackets="+({initiator_packets}[^"]+)"+""",
    """ResponderPackets="+({responder_packets}\d+)"+""",
    """User="+(No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+""",
  ]
  DupFields = [ "result->action" ]


}
```