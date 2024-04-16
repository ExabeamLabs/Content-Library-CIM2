#### Parser Content
```Java
{
Name = "catonetworks-cc-json-vpn-http-success-monitor"
Conditions = [
  """"event_sub_type":""""
  """"action":"Monitor""""
  """"event_type":"Security""""
]
ParserVersion = "v1.0.0"

json-catonetwork = {
  Vendor = "CatoNetworks"
  Product = "Cato Cloud"
  ExtractionType = json
  TimeFormat = "epoch"
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.src_country,exa_field_name=src_country""",
    """exa_json_path=$.dest_country,exa_field_name=dest_country""",
    """exa_json_path=$.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.dest_port,exa_field_name=dest_port""",
    """exa_json_path=$.src_port,exa_field_name=src_port""",
    """exa_json_path=$.categories,exa_field_name=categories""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.domain_name,exa_field_name=domain""",
    """exa_json_path=$.http_host_name,exa_field_name=host"""
    """exa_json_path=$.vpn_user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.event_type,exa_field_name=event_category"""
    """exa_json_path=$.event_sub_type,exa_field_name=sub_category"""
  
}
```