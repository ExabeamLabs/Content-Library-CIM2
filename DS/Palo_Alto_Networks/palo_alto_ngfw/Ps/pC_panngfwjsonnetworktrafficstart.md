#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-start
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [  """"LogType":"DECRYPTION"""", """"SubType":"start"""", """"FromZone":"""", """"ToZone":"""" ]
  ExtractionType = json
  Fields = [
  """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.PrivateIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.PrivateIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.PublicIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PublicIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.LogType,exa_field_name=app"""
  """exa_json_path=$.EventStatus,exa_field_name=result"""
  """exa_json_path=$.EndpointDeviceName,exa_field_name=src_host"""
  """exa_json_path=$.SourceRegion,exa_field_name=src_country"""
  """exa_json_path=$.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  """exa_json_path=$.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.EventIDValue,exa_field_name=auth_method"""
  """exa_json_path=$.SourcePort,exa_field_name=src_port"""
  """exa_json_path=$.DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$.Protocol,exa_field_name=protocol"""
  """exa_json_path=$.LogType,exa_field_name=event_name"""
  """exa_json_path=$.EndpointOSVersion,exa_field_name=os"""
  """exa_regex=Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.SourceUser,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.SourceAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.NATSource,exa_regex=({src_translated_ip}[a-fA-F\d:.]+)"""
  """exa_json_path=$.NATDestination,exa_regex=({dest_translated_ip}[a-fA-F\d:.]+)"""
  """exa_json_path=$.NATSourcePort,exa_field_name=src_translated_port"""
  """exa_json_path=$.NATDestinationPort,exa_field_name=dest_translated_port"""
  """exa_json_path=$.SubType,exa_field_name=operation"""
  """exa_json_path=$.Action,exa_field_name=result"""
  """exa_json_path=$.Rule,exa_field_name=rule"""
  """exa_json_path=$.PolicyName,exa_field_name=additional_info"""
  """exa_json_path=$.FromZone,exa_field_name=src_network_zone"""
  """exa_json_path=$.ToZone,exa_field_name=dest_network_zone"""
  ]
  ParserVersion = "v1.0.0"


}
```