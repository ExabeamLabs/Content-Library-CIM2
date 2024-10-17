#### Parser Content
```Java
{
Name = illumio-ic-json-endpoint-authentication-fail-requestauthentication_failed
  ParserVersion = v1.0.0
  Vendor = Illumio
  Product = Illumio Core
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """.illum.io""", """"info":{""", """"event_type":"""", """"request.authentication_failed"""" ]
  Fields = [
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.pce_fqdn,exa_field_name=web_domain"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.info.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event_type,exa_field_name=event_name"""
    """exa_json_path=$.href,exa_field_name=uri_path"""
    """exa_json_path=$.notifications.uuid,exa_field_name=user_uid"""
    """exa_json_path=$.info.api_endpoint,exa_field_name=url"""
    """exa_json_path=$.info.api_method,exa_field_name=method"""
    """exa_json_path=$.status,exa_field_name=method"""    
  ]
}  
]
#============================================== End of DefaultParsersAA section ==================================================================
#============================================== Start of DefaultParsersDL section ==================================================================
DefaultParsersDL = [

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