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
    """(\w+\s\d+\s\d+:\d+:\d+)\s(|({host}[^\s]+))\s({event_name}RT_FLOW: [^:]+):\s({failure_reason}session denied)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)->({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)(\s({result}[^\s]+))?\s((None)|(junos-)?({service_name}[^\s]+))\s((N\/A)|({protocol_id}[^\s]+))\s((N\/A)|({policy_name}[^\s]+))\s((N\/A)|({src_network_zone}[^\s]+))\s((N\/A)|({dest_network_zone}[^\s]+))\s((UNKNOWN)|({network_app}[^\s]+))\s((UNKNOWN)|({subtype}[^\s]+))\s((N\/A)|({user}[\w\.\-]{1,40}\$?))\(\S+\)\s({src_interface}[^\s]+)\s((UNKNOWN)|No|({additional_info}[^\s]+))\s(\S+\s)?({action}(?i)(denied|deny))"""
  ]


}
```