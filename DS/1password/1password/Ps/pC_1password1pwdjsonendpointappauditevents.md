#### Parser Content
```Java
{
Name = 1password-1pwd-json-endpoint-app-audit-events
  ParserVersion = v1.0.0
  Vendor = 1password
  Product = 1password
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ"
  Conditions = [ """"uuid":""", """"object_type":""", """"account_uuid":""", """"actor_details":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.actor_uuid,exa_field_name=user_uid""",
    """exa_json_path=$.actor_details.email,exa_field_name=email_address""",
    """exa_json_path=$.actor_details.name,exa_field_name=full_name""",
    """exa_json_path=$.location.region,exa_field_name=location_state""",
    """exa_json_path=$.location.city,exa_field_name=location_city""",
    """exa_json_path=$.location.country,exa_field_name=country""",
    """exa_json_path=$.session.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.object_type,exa_field_name=operation""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.session.uuid,exa_field_name=session_id""",
    """exa_json_path=$.source,exa_field_name=app""",
    """exa_json_path=$.date,exa_field_name=time""",
    """exa_json_path=$.attributes.aux_details.uuid,exa_field_name=user_uid""",
    """exa_json_path=$.attributes.object_type,exa_field_name=object_type""",
    """exa_json_path=$.attributes.session.uuid,exa_field_name=session_id""",
    """exa_json_path=$.attributes.network.client.geoip.city.name,exa_field_name=location_city""",
    """exa_json_path=$.attributes.network.client.geoip.subdivision.name,exa_field_name=location_state""",
    """exa_json_path=$.attributes.network.client.geoip.country.name,exa_field_name=country""",
    """exa_json_path=$.attributes.network.client.ip,exa_field_name=src_ip""",
    """exa_json_path=$.attributes.object_details.email,exa_field_name=dest_email_address""",
    """exa_json_path=$.attributes.usr.email,exa_field_name=email_address""",
    """exa_json_path=$.attributes.usr.name,exa_field_name=full_name""",
    """exa_json_path=$.attributes.evt.type,exa_field_name=operation""",
    """exa_json_path=$.attributes.evt.name,exa_field_name=action""",
  ]


}
```