#### Parser Content
```Java
{
Name = "cisco-fp-kv-network-traffic-estreamer"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" SFIMS: """
"""Protocol:"""
"""AccessControlRuleName:"""
"""AccessControlRuleAction:"""
"""DNSResponseType:"""
  ]
  Fields = [
"""({host}[\w\.-]+)\s+SFIMS:"""
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""\WProtocol:\s*({protocol}[^,]+)"""
"""\WSrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WDstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\WSrcPort:\s*({src_port}\d+)"""
"""\WDstPort:\s*({dest_port}\d+)"""
"""\WIngressZone:\s*({ingress_zone}[^,]+)"""
"""\WEgressZone:\s*({egress_zone}[^,]+)"""
"""\WPolicy:\s*({policy_name}[^,]+)"""
"""\WConnectType:\s*({connection_type}[^,]+)"""
"""\WAccessControlRuleName:\s*(Unknown|({rule}[^,]+))"""
"""\WAccessControlRuleAction:\s*({result}[^,]+)"""
"""\WUserName:\s*(No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""\WInitiatorPackets:\s*({initiator_packets}[^,]+)"""
"""\WResponderPackets:\s*({responder_packets}\d+)"""
"""\WInitiatorBytes:\s*({bytes_in}\d+)"""
"""\WResponderBytes:\s*({bytes_out}\d+)"""
"""\WNAPPolicy:\s*({nap_policy}[^,]+)"""
"""\WDNSResponseType:\s*({response_type}[^,]+)"""
"""\WTCPFlags:\s*({tcp_flags}[^,]+?)(,|\s*$)"""
"""\WURLCategory:\s*(Unknown|({category}[^,]+?))(,|\s*$)"""
"""\WURLReputation:\s*({reputation}[^,]+?)(,|\s*$)"""
"""exa_regex=({host}[\w\.-]+)\s+SFIMS:"""
"""exa_regex=\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""exa_json_path=$.message,exa_regex=\WProtocol:\s*({protocol}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WSrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.message,exa_regex=\WDstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""exa_json_path=$.message,exa_regex=\WSrcPort:\s*({src_port}\d+)"""
"""exa_json_path=$.message,exa_regex=\WDstPort:\s*({dest_port}\d+)"""
"""exa_json_path=$.message,exa_regex=\WIngressZone:\s*({ingress_zone}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WEgressZone:\s*({egress_zone}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WPolicy:\s*({policy_name}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WConnectType:\s*({connection_type}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WAccessControlRuleName:\s*(Unknown|({rule}[^,]+))"""
"""exa_json_path=$.message,exa_regex=\WAccessControlRuleAction:\s*({result}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WUserName:\s*(No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""exa_json_path=$.message,exa_regex=\WInitiatorPackets:\s*({initiator_packets}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WResponderPackets:\s*({responder_packets}\d+)"""
"""exa_json_path=$.message,exa_regex=\WInitiatorBytes:\s*({bytes_in}\d+)"""
"""exa_json_path=$.message,exa_regex=\WResponderBytes:\s*({bytes_out}\d+)"""
"""exa_json_path=$.message,exa_regex=\WNAPPolicy:\s*({nap_policy}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WDNSResponseType:\s*({response_type}[^,]+)"""
"""exa_json_path=$.message,exa_regex=\WTCPFlags:\s*({tcp_flags}[^,]+?)(,|\s*$)"""
"""exa_json_path=$.message,exa_regex=\WURLCategory:\s*(Unknown|({category}[^,]+?))(,|\s*$)"""
"""exa_json_path=$.message,exa_regex=\WURLReputation:\s*({reputation}[^,]+?)(,|\s*$)"""
  ]
  DupFields = [ "result->action" ]


}
```