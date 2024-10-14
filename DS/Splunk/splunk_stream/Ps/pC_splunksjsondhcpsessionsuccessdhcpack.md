#### Parser Content
```Java
{
Name = splunk-s-json-dhcp-session-success-dhcpack
  ExtractionType = json
  Vendor = Splunk 
  Product = Splunk Stream
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"opcode":"""", """"DHCPACK"""", """ip:udp:dhcp""", """"giaddr":"""", """"flow_id":"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.bytes,exa_field_name=bytes"""
    """exa_json_path=$.bytes_in,exa_field_name=bytes_in"""
    """exa_json_path=$.bytes_out,exa_field_name=bytes_out"""
    """exa_json_path=$.dest_ip,exa_field_name=dest_ip"""
    """exa_json_path=$.dest_mac,exa_field_name=dest_mac"""
    """exa_json_path=$.dest_port,exa_field_name=dest_port"""
    """exa_json_path=$.dns_server,exa_field_name=dns_ip_flow"""
    """exa_json_path=$.domain_name.[1],exa_field_name=domain"""
    """exa_json_path=$.opcode,exa_field_name=event_name"""
    """exa_json_path=$.router,exa_field_name=router_ip_flow"""
    """exa_json_path=$.src_ip,exa_field_name=src_ip"""
    """exa_json_path=$.src_mac,exa_field_name=src_mac"""
    """exa_json_path=$.src_port,exa_field_name=src_port"""
    """exa_json_path=$.subnetmask,exa_field_name=router_subnet"""
    """exa_json_path=$.transaction_id,exa_field_name=transaction_id"""
    """exa_regex=({protocol}dhcp)""",
    """exa_json_path=$.yiaddr,exa_field_name=assigned_ip"""
    """exa_json_path=$.ip_lease_time,exa_field_name=ip_lease_time"""
    """exa_json_path=$.host_name,exa_field_name=host"""
    ]
    DupFields = ["transaction_id->trans_id"]
  ParserVersion = "v1.0.0"


}
```