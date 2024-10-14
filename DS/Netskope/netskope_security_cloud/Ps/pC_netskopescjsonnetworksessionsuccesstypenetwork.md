#### Parser Content
```Java
{
Name = "netskope-sc-json-network-session-success-typenetwork"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"type":"network"""", """"flow_status":""", """"ccl":"""", """"traffic_type":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.userip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.os,exa_field_name=os,exa_match_expr=!InList(toLower($.os),"unknown")"""
    """exa_json_path=$.access_method,exa_field_name=auth_method"""
    """exa_json_path=$.dst_location,exa_field_name=location"""
    """exa_json_path=$.dst_country,exa_field_name=dest_country"""
    """exa_json_path=$.dstport,exa_field_name=dest_port"""
    """exa_json_path=$.policy,exa_field_name=additional_info"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.traffic_type,exa_field_name=app_type"""
    """exa_json_path=$.ip_protocol,exa_field_name=protocol"""
    """exa_json_path=$.client_bytes,exa_field_name=bytes_in"""
    """exa_json_path=$.server_bytes,exa_field_name=bytes_out"""
    """exa_json_path=$.flow_status,exa_field_name=result"""
  ]
  ParserVersion = "v1.0.0"


}
```