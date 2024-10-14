#### Parser Content
```Java
{
Name = "catonetwork-cc-json-vpn-login-success-reconnected"
Vendor = "CatoNetworks"
Product = "Cato Cloud"
ExtractionType = json
TimeFormat = [ "epoch" ]
Conditions = [ """"event_sub_type":""", """"Reconnected"""", """"link_type":""", """"Cato"""", """"event_type":""", """"Connectivity""""]
Fields = [
    """exa_json_path=$.event_type,exa_field_name=event_category""",
    """exa_json_path=$.src_country_code,exa_field_name=src_country_code""",
    """exa_json_path=$.tunnel_protocol,exa_field_name=tunnel_protocol""",
    """exa_json_path=$.event_sub_type,exa_field_name=event_subtype""",
    """exa_json_path=$.account_id,exa_field_name=account_id""",
    """exa_json_path=$.src_country,exa_field_name=src_country""",
    """exa_json_path=$.time,exa_field_name=time"""
]
ParserVersion = "v1.0.0"


}
```