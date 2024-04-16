#### Parser Content
```Java
{
Name = "cisco-fp-kv-dns-request-success-connection-stats"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """fw_rule_action=""", """rec_type_desc="Connection Statistics"""", """event_desc="Flow Statistics"""", """app_proto=DNS""" ]
  Fields = [
    """event_sec=({time}\d{10})""",
    """url="({url}[^"]+)"""",
    """connection_id=({connection_id}\d+)""",
    """http_referrer="(|({referrer}[^"]+))"""",
    """http_response=({http_response_code}\d+)""",
    """sec_zone_egress=(Unknown|N\/A|({egress_zone}[^=]+?))\s\w+=""",
    """sec_zone_ingress=(Unknown|N\/A|({ingress_zone}[^=]+?))\s\w+=""",
    """iface_ingress=({ingress_interface}[^=]+?)\s\w+=""",
    """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?""",
    """dest_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=dest_port}\d+))?""",
    """src_port=({src_port}\d+)""",
    """dest_port=({dest_port}\d+)""",
    """src_bytes=({bytes_in}\d+)""",
    """dest_bytes=({bytes_out}\d+)""",
    """fw_policy="*({policy_name}[^"=]+?)"*\s\w+=""",
    """fw_rule="*({rule}[^"=]+?)"*\s\w+=""",
    """ip_proto=({protocol}[^\s]+)""",
    """fw_rule_action=({action}[^\s]+)""",
    """rec_type_desc="({event_name}[^"]+)"""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """sensor=({host}[\w\-\.]+)""",
    """src_ip_country="*({src_country}[^"=]+?)"*\s\w+=""",
    """dest_ip_country="*({dest_country}[^"=]+?)"*\s\w+=""",
    """app_proto=(Unknown|({app_protocol}[^\s]+))""",
    """dns_query=({dns_query}[^=]+?)\s\w+=""",
    """dns_record_name=({dns_query_type}[^=]+?)\s\w+=""",
    """dns_ttl=({response_ttl}\d+)"""
  ]


}
```