#### Parser Content
```Java
{
Name = portnox-clear-json-endpoint-authentication-fail-radius
  ParserVersion = v1.0.0
  Conditions = [ """Portnox""", """CLEAR""", """"category":"Access"""", """"RADIUS failed to authenticate device""" ]

portnox-clear-json = {
  ExtractionType = json
  Vendor = "Portnox"
  Product = "Portnox CLEAR"
  TimeFormat = "epoch"
  Fields = [
    """exa_json_path=$..time,exa_field_name=time""",
    """exa_json_path=$.account,exa_field_name=account""",
    """exa_json_path=$.name,exa_field_name=event_name""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.hostName,exa_field_name=host""",
    """exa_json_path=$..alertId,exa_field_name=alert_id""",
    """exa_json_path=$..source,exa_field_name=device_name""",
    """exa_json_path=$..sourceId,exa_field_name=device_id""",
    """exa_json_path=$..ip,exa_field_name=device_ip""",
    """exa_json_path=$..mac,exa_field_name=src_mac""",
    """exa_json_path=$..category,exa_field_name=category""",
    """exa_json_path=$..description,exa_field_name=additional_info""",
    """exa_json_path=$..policy,exa_field_name=policy_name""",
    """exa_json_path=$..network,exa_field_name=network""",
    """exa_json_path=$..site,exa_field_name=site_name"""
    """exa_json_path=$..nas,exa_field_name=framed_addr"""
    """exa_regex="authNType":"(unknown|({auth_type}[^",]+))""""
    """exa_regex=NAS IP '({nas_ip_address}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_regex=User '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'"""
    
}
```