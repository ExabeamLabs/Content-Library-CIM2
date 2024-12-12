#### Parser Content
```Java
{
Name = "catonetworks-cc-json-vpn-http-success-sdp"
Conditions = [
  """"event_sub_type":"""
  """"action":"""
  """"SDP """
  """"event_type":"""
  """"Security""""
]
ParserVersion = "v1.0.0"

json-catonetwork = {
  Vendor = "CatoNetworks"
  Product = "Cato Cloud"
  ExtractionType = json
  TimeFormat = "epoch"
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.fieldsMap.time,exa_field_name=time""",
    """exa_json_path=$..src_country,exa_field_name=src_country""",
    """exa_json_path=$..dest_country,exa_field_name=dest_country""",
    """exa_json_path=$..dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$..src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..dest_port,exa_field_name=dest_port""",
    """exa_json_path=$..src_port,exa_field_name=src_port""",
    """exa_json_path=$..categories,exa_field_name=categories""",
    """exa_json_path=$..action,exa_field_name=action""",
    """exa_json_path=$..domain_name,exa_field_name=web_domain""",
    """exa_json_path=$..http_host_name,exa_field_name=host"""
    """exa_json_path=$..vpn_user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$..event_type,exa_field_name=event_category"""
    """exa_json_path=$..ip_protocol,exa_field_name=protocol""",
    """exa_json_path=$..application,exa_field_name=app""",
    """exa_json_path=$..application_id,exa_field_name=app""",
    """exa_json_path=$..application_name,exa_field_name=app""",
    """exa_json_path=$..user_id,exa_field_name=user_id""",
    """exa_json_path=$..dest_user_id,exa_field_name=dest_user_id""",
    """exa_json_path=$..os_version,exa_field_name=os_version""",
    """exa_json_path=$..os_type,exa_field_name=os""",
    """exa_json_path=$..account_id,exa_field_name=account_id""",
    """exa_json_path=$..event_sub_type,exa_field_name=event_subtype""",
    """exa_json_path=$..rule_id,exa_field_name=rule_id""",
    """exa_json_path=$..app_stack,exa_field_name=apps""",
    """exa_json_path=$..host_mac,exa_field_name=src_mac""",
    """exa_json_path=$..host_ip,exa_field_name=src_ip""",
    """exa_json_path=$..socket_interface,exa_field_name=src_interface""",
    """exa_json_path=$..event_message,exa_field_name=additional_info""",
    """exa_json_path=$..account_id,exa_field_name=account_id"""
  
}
```