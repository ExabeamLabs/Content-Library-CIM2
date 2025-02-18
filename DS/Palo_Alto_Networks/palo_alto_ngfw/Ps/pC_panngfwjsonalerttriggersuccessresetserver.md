#### Parser Content
```Java
{
Name = pan-ngfw-json-alert-trigger-success-resetserver
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """"LogType":"THREAT"""", """"Subtype":"virus"""", """"Action":"reset-server"""" ]
  Fields = [
  """exa_json_path=$.event.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.event.DeviceName,exa_field_name=host"""
  """exa_json_path=$..DeviceName,exa_field_name=device_name"""
  """exa_json_path=$.event.PrivateIPv4,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PrivateIPv6,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.LogType,exa_field_name=app"""
  """exa_json_path=$.event.EventStatus,exa_field_name=result"""
  """exa_json_path=$.event.EndpointDeviceName,exa_field_name=src_host"""
  """exa_json_path=$.event.SourceRegion,exa_field_name=src_country,exa_match_expr=!Contains(toLower($.SourceRegion),"null")"""
  """exa_json_path=$.event.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.event.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=auth_method,exa_match_expr=!Contains(toLower($.EventIDValue),"null")"""
  """exa_json_path=$.event.Description,exa_regex=({additional_info}[^"]+:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))"""
  """exa_json_path=$..Application,exa_field_name=network_app"""
	"""exa_json_path=$..InboundInterface,exa_field_name=src_interface"""
  """exa_json_path=$..OutboundInterface,exa_field_name=dest_interface"""
  """exa_json_path=$..FromZone,exa_field_name=src_network_zone"""
  """exa_json_path=$..ToZone,exa_field_name=dest_network_zone"""
  """exa_json_path=$..NATSource,exa_field_name=src_translated_ip"""
  """exa_json_path=$..NATDestination,exa_field_name=dest_translated_ip"""
  ]
  ParserVersion = "v1.0.0"


}
```