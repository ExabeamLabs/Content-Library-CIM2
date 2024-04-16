#### Parser Content
```Java
{
Name = pan-ngfw-json-network-traffic-fail-actiondrop
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"LogType":"TRAFFIC"""", """"Action":"drop""", """"Subtype":"drop"""", """"Rule":"""" ]
  ExtractionType = json
  Fields = [
  """exa_json_path=$.event.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.event.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.event.DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.event.PrivateIPv4,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PrivateIPv6,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_regex=Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.SourcePort,exa_field_name=src_port"""
  """exa_json_path=$.event.DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$.event.Protocol,exa_field_name=protocol"""
    """exa_json_path=$.event.Action,exa_field_name=action"""
    """exa_json_path=$.event.NATSource,exa_regex=({src_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.event.NATDestination,exa_regex=({dest_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.event.NATSourcePort,exa_field_name=src_translated_port"""
    """exa_json_path=$.event.NATDestinationPort,exa_field_name=dest_translated_port"""
    """exa_json_path=$.event.Bytes,exa_field_name=bytes"""
    """exa_json_path=$.event.BytesSent,exa_field_name=bytes_out"""
    """exa_json_path=$.event.BytesReceived,exa_field_name=bytes_in"""
    """exa_json_path=$.event.URLCategory,exa_field_name=category"""
    """exa_json_path=$.event.VendorSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.event.LogType,exa_field_name=event_category"""
      """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.PrivateIPv4,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PrivateIPv6,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PublicIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PublicIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_regex=Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.SourcePort,exa_field_name=src_port"""
  """exa_json_path=$.DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$.Protocol,exa_field_name=protocol"""
    """exa_json_path=$.Action,exa_field_name=action"""
    """exa_json_path=$.NATSource,exa_regex=({src_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.NATDestination,exa_regex=({dest_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.NATSourcePort,exa_field_name=src_translated_port"""
    """exa_json_path=$.NATDestinationPort,exa_field_name=dest_translated_port"""
    """exa_json_path=$.Bytes,exa_field_name=bytes"""
    """exa_json_path=$.BytesSent,exa_field_name=bytes_out"""
    """exa_json_path=$.BytesReceived,exa_field_name=bytes_in"""
    """exa_json_path=$.URLCategory,exa_field_name=category"""
    """exa_json_path=$.VendorSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.LogType,exa_field_name=event_category"""
    
  ]


}
```