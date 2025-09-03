#### Parser Content
```Java
{
Name = "pan-ngfw-json-http-session-webbrowsing"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""LogType":"THREAT""""
""""HTTPMethod":"""
""""URL":"""
""""Subtype":"url""""
""""Application":"web-browsing""""
]
Fields = [
  """exa_json_path=$..TimeGenerated,exa_field_name=time"""
  """exa_json_path=$..DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.event.PrivateIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PrivateIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PublicIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$..SourceUser,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$..SourceAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$..SourcePort,exa_field_name=src_port"""
  """exa_json_path=$..DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$..DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$..HTTPMethod,exa_field_name=method"""
  """exa_json_path=$..Action,exa_field_name=action"""
  """exa_json_path=$..URL,exa_regex=({url}({web_domain}[^"\/\?]+)({uri_path}\/[^?"]*)?({uri_query}\?[^"]+)?)"""
  """exa_json_path=$..Referer,exa_field_name=referrer"""
  """exa_json_path=$..Protocol,exa_field_name=protocol"""
  """exa_json_path=$..UserAgent,exa_field_name=user_agent"""
  """exa_json_path=$..URLCategoryList,exa_field_name=categories"""
  """exa_json_path=$..URLCategory,exa_field_name=category"""
  """exa_json_path=$..ContentType,exa_field_name=mime"""
  """exa_json_path=$..DirectionOfAttack,exa_field_name=direction"""
  """exa_json_path=$..NATSource,exa_field_name=src_translated_ip"""
  """exa_json_path=$..NATDestination,exa_field_name=dest_translated_ip"""
  """exa_json_path=$..NATSourcePort,exa_field_name=src_translated_port"""
  """exa_json_path=$..NATDestinationPort,exa_field_name=dest_translated_port"""
  """exa_json_path=$..Application,exa_field_name=network_app"""
	"""exa_json_path=$..InboundInterface,exa_field_name=src_interface"""
  """exa_json_path=$..OutboundInterface,exa_field_name=dest_interface"""
  """exa_json_path=$..FromZone,exa_field_name=src_network_zone"""
  """exa_json_path=$..ToZone,exa_field_name=dest_network_zone"""
  """exa_json_path=$..DeviceName,exa_field_name=device_name"""
]
ParserVersion = "v1.0.0"


}
```