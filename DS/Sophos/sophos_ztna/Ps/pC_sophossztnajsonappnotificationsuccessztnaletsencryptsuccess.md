#### Parser Content
```Java
{
Name = sophos-sztna-json-app-notification-success-ztnaletsencryptsuccess
  Product = Sophos ZTNA
  Conditions = [ """"Event::ZTNA::ZTNALetsEncryptSuccess"""", """"type":""" ]
  ParserVersion = "v1.0.0"

sophos-notification-events = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.when,exa_field_name=time""",
  	"""exa_json_path=$.source,exa_regex=(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\s]+\s[^"]+)$|((({domain}[^\\"]+?))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$)""",
  	"""exa_json_path=$.location,exa_regex=^({host}[\w\-\.]+)$""",
  	"""exa_json_path=$.id,exa_field_name=event_id""",
  	"""exa_json_path=$.severity,exa_field_name=severity""",
  	"""exa_json_path=$.name,exa_field_name=event_name""",
  	"""exa_json_path=$.type,exa_field_name=event_subtype""",
  	"""exa_json_path=$.description,exa_field_name=additional_info""",
  	"""exa_json_path=$..endpoint_type,exa_field_name=device_type""",
  	"""exa_json_path=$.user_id,exa_field_name=user_id""",
    """exa_json_path=$.group,exa_field_name=group_type""",
  	"""exa_json_path=$..source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.location,exa_regex=^({src_host}[\w\-\.]+)$""",
  
}
```