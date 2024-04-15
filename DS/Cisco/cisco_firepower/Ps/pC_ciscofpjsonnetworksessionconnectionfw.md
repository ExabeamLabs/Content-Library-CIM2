#### Parser Content
```Java
{
Name = "cisco-fp-json-network-session-connection-fw"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"originator_type":"FTD"""",
  """"firewall_rule_list":"""
]
Fields = [
""""first_packet_second":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
""""device_uuid":"({device_id}[^"]+)""""
""""context":"({additional_info}[^"]+)""""
""""ingress_interface":"({dest_interface}[^"]+)""""
""""ingress_zone":"({ingress_zone}[^"]+)""""
""""egress_interface":"({src_interface}[^"]+)""""
""""egress_zone":"({egress_zone}[^"]+)""""
""""initiator_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
""""initiator_port":({src_port}\d+)"""
""""initiator_packets":({initiator_packets}\d+)"""
""""initiator_bytes":({bytes_out}\d+)"""
""""responder_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
""""responder_port":({dest_port}\d+)"""
""""responder_packets\s*":\s*({responder_packets}\d+)"""
""""responder_bytes":({bytes_in}\d+)"""
""""protocol":"({protocol}[^"]+)""""
""""tcp_flags":({tcp_flags}\d+)"""
""""dns_response_type":"({dns_response_code}[^"]+)""""
""""client_application":"({network_app}[^"]+)""""
""""firewall_policy":"({policy_name}[^"]+)""""
""""firewall_rule_list":"({rule}[^"]+)""""
""""nap_policy":"({nap_policy}[^"]+)""""
""""ac_rule_action":"({result}[^"]+)""""
""""ssl_actual_action":"({action}[^"]+)""""
""""url":"({url}[^"]+)""""
""""url_category":"({category}[^"]+)""""
""""url_reputation":"({reputation}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```