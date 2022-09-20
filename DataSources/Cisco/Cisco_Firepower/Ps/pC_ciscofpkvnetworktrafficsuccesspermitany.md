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
    """({host}[\w\-.]+)\s*%FTD-""",
    """%FTD-({priority}\d+)-({event_code}\d+)\\?""",
    """({event_name}Permit Any)""",
    """AccessControlRuleAction="+({action}[^"]+)"+""",
    """SrcIP="+({src_ip}[^"]+)"+""",
    """DstIP="+({dest_ip}[^"]+)"+""",
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
    """User="+(No Authentication Required|({user}[^"]+))"+""",
  ]


}
```