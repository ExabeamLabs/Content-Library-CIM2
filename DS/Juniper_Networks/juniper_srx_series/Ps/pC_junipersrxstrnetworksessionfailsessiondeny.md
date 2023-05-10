#### Parser Content
```Java
{
Name = juniper-srx-str-network-session-fail-sessiondeny
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ 
"""RT_FLOW: RT_FLOW_SESSION_DENY"""
"""session denied"""
]
  Fields = [
    """(\w+\s\d+\s\d+:\d+:\d+)\s(|({host}[^\s]+))\s({event_name}RT_FLOW: [^:]+):\s({failure_reason}session denied)\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/({src_port}\d+)->({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/({dest_port}\d+)(\s({result}[^\s]+))?\s((None)|(junos-)?({service_name}[^\s]+))\s((N\/A)|({protocol_id}[^\s]+))\s((N\/A)|({policy_name}[^\s]+))\s((N\/A)|({src_network_zone}[^\s]+))\s((N\/A)|({dest_network_zone}[^\s]+))\s((UNKNOWN)|({network_app}[^\s]+))\s((UNKNOWN)|({subtype}[^\s]+))\s((N\/A)|({user}[^\s]+))\(\S+\)\s({src_interface}[^\s]+)\s((UNKNOWN)|No|({additional_info}[^\s]+))\s(\S+\s)?({action}(?i)(denied|deny))"""
  ]


}
```