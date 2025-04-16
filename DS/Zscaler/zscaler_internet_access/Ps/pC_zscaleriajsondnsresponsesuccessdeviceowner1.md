#### Parser Content
```Java
{
Name = zscaler-ia-json-dns-response-success-deviceowner-1
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [ """"department":"""", """"location":"""", """"device_owner":"""", """"device_hostname":"""", """"dns_response":"""" ]
  Fields=[
    """exa_json_path=$.datetime,exa_field_name=time""",
    """exa_json_path=$.device_hostname,exa_field_name=host""",
    """exa_json_path=$.user,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.department,exa_field_name=department""",
    """exa_json_path=$.location,exa_field_name=location""",
    """exa_json_path=$.response_action,exa_field_name=result""",
    """exa_json_path=$.response_rule_label,exa_field_name=rule""",
    """exa_json_path=$.dns_request_type,exa_field_name=dns_query_type""",
    """exa_json_path=$.dns_response,exa_field_name=dns_response""",
    """exa_json_path=$.dns_request,exa_field_name=dns_query""",
    """exa_json_path=$.dest_port,exa_field_name=dest_port""",
    """exa_json_path=$.dest_ip,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
    """exa_json_path=$.src_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.durationms,exa_field_name=duration""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.device_owner,exa_field_name=owner_id"""
  ]
  ParserVersion = "v1.0.0"


}
```