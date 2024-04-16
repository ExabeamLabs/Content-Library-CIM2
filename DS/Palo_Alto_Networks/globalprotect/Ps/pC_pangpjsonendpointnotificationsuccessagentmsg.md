#### Parser Content
```Java
{
Name = pan-gp-json-endpoint-notification-success-agentmsg
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """"EventStatus":"success"""", """"AuthMethod":""", """Stage":"agent-msg"""", """GLOBALPROTECT""", """"EventIDValue":"gateway-agent-msg"""" ]
  Fields = [
  """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.DeviceName,exa_field_name=host"""
  """exa_json_path=$.PrivateIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PrivateIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PublicIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PublicIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.LogType,exa_field_name=app"""
  """exa_json_path=$.EventStatus,exa_field_name=result"""
  """exa_json_path=$.EndpointDeviceName,exa_field_name=src_host,exa_match_expr=!Contains(toLower($.EndpointDeviceName),"null")"""
  """exa_json_path=$.SourceRegion,exa_field_name=src_country,exa_match_expr=!Contains(toLower($.SourceRegion),"null")"""
  """exa_json_path=$.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  """exa_json_path=$.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.EventIDValue,exa_field_name=auth_method,exa_match_expr=!Contains(toLower($.SourceRegion),"null")"""
  """exa_json_path=$.Description,exa_field_name=additional_info"""
  ]
  ParserVersion = v1.0.0


}
```