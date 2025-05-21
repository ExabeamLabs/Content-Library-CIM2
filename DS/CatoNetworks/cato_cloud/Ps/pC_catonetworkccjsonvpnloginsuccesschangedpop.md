#### Parser Content
```Java
{
Name = "catonetwork-cc-json-vpn-login-success-changedpop"
Vendor = "CatoNetworks"
Product = "Cato Cloud"
ExtractionType = json
TimeFormat = [ "epoch" ]
Conditions = [ """"event_sub_type":""", """"Changed Pop"""", """"link_type":""", """"Cato"""", """"event_type":""", """"Connectivity"""", """"vpn_user_email":""""]
Fields = [
    """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.device_name,exa_field_name=host""",
    """exa_json_path=$.event_type,exa_field_name=event_category""",
    """exa_json_path=$.src_country_code,exa_field_name=src_country_code""",
    """exa_json_path=$.vpn_user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.client_version,exa_field_name=client_version""",
    """exa_json_path=$.tunnel_protocol,exa_field_name=tunnel_protocol""",
    """exa_json_path=$.os_version,exa_field_name=os_version""",
    """exa_json_path=$.event_sub_type,exa_field_name=event_subtype""",
    """exa_json_path=$.account_id,exa_field_name=account_id""",
    """exa_json_path=$.user_id,exa_field_name=user_id""",
    """exa_json_path=$.src_country,exa_field_name=src_country""",
    """exa_json_path=$.os_type,exa_field_name=os""",
    """exa_json_path=$.time,exa_field_name=time"""
]
ParserVersion = "v1.0.0"


}
```