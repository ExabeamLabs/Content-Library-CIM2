#### Parser Content
```Java
{
Name = "catonetwork-cc-json-network-notification-success-routing"
Vendor = "CatoNetworks"
Product = "Cato Cloud"
ExtractionType = json
TimeFormat = [ "epoch" ]
Conditions = [ """"event_type":""", """"Routing"""", """"event_sub_type":""", """"VPN Never-Off Bypass"""" ]
Fields = [
    """exa_json_path=$.event_type,exa_field_name=event_category""",
    """exa_json_path=$.vpn_user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.client_version,exa_field_name=client_version""",
    """exa_json_path=$.event_sub_type,exa_field_name=event_subtype""",
    """exa_json_path=$.account_id,exa_field_name=account_id""",
    """exa_json_path=$.user_id,exa_field_name=user_id""",
    """exa_json_path=$.os_type,exa_field_name=os""",
    """exa_json_path=$.time,exa_field_name=time"""
]
ParserVersion = "v1.0.0"


}
```