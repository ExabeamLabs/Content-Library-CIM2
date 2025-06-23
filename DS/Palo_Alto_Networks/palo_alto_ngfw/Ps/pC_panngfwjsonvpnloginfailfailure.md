#### Parser Content
```Java
{
Name = "pan-ngfw-json-vpn-login-fail-failure"
Conditions = [
""""LogType":"GLOBALPROTECT""""
""""DeviceSN":""""
""""EventStatus":"failure""""
]
ParserVersion = "v1.0.0"

paloalto-vpn.Fields}[
    """exa_json_path=$.event.Action,exa_field_name=action"""
    """exa_json_path=$.event.VendorSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.event.LogType,exa_field_name=alert_type"""
    """exa_json_path=$.event.Subtype,exa_field_name=alert_type"""
    """exa_json_path=$.event.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.event.ThreatCategory,exa_regex=((?i:unknown)|({threat_category}[^"]+))"""
    """exa_json_path=$.event.ThreatID,exa_regex=({alert_name}[^"\(]+?)\s*(\(({alert_id}[^"\)]\d+))"""
    """exa_json_path=$..Application,exa_field_name=network_app"""
	  """exa_json_path=$..InboundInterface,exa_field_name=src_interface"""
    """exa_json_path=$..OutboundInterface,exa_field_name=dest_interface"""
    """exa_json_path=$..FromZone,exa_field_name=src_network_zone"""
    """exa_json_path=$..ToZone,exa_field_name=dest_network_zone"""
    """exa_json_path=$..NATSource,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$..NATDestination,exa_regex=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$..DeviceName,exa_field_name=device_name"""
  ]
Name = pan-ngfw-json-alert-trigger-success-vulnerability-1
Conditions = [
  """"LogType":"THREAT""""
  """"Subtype":"vulnerability""""
  """"Action":"alert""""
]
DupFields = ["alert_name -> alert_subject"]
ParserVersion = "v1.0.0"
},

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
{
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Fields = [
  """exa_json_path=$..TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$..DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$..DeviceName,exa_field_name=device_name"""
  """exa_json_path=$.event.PrivateIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PrivateIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PublicIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$..LogType,exa_field_name=app"""
  """exa_json_path=$.event.EventStatus,exa_field_name=result"""
  """exa_json_path=$.event.EndpointDeviceName,exa_field_name=src_host"""
  """exa_json_path=$.event.SourceRegion,exa_field_name=src_country"""
  """exa_json_path=$.event.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.event.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=auth_method"""
  """exa_json_path=$..SourcePort,exa_field_name=src_port"""
  """exa_json_path=$..DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$..Protocol,exa_field_name=protocol"""
  """exa_json_path=$.event.EndpointOSVersion,exa_field_name=os"""
  """exa_regex=Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.Description,exa_field_name=additional_info"""
  """exa_json_path=$..LogType,exa_field_name=event_category"""
  """exa_json_path=$..Action,exa_field_name=action"""
  """exa_regex=({alert_name}spyware)"""
  """exa_json_path=$..VendorSeverity,exa_field_name=alert_severity"""
  """exa_json_path=$..Subtype,exa_field_name=alert_type"""
  """exa_json_path=$..DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.event.ThreatCategory,exa_regex=((?i:unknown)|({threat_category}[^"]+))"""
  """exa_json_path=$.event.ThreatID,exa_regex=({alert_name}[^"\(]+?)\s*(\(({alert_id}[^"\)]\d+))"""
  """exa_json_path=$..Application,exa_field_name=app"""
  """exa_json_path=$.event.FileName,exa_field_name=file_name"""
  """exa_json_path=$..NATSource,exa_regex=({src_translated_ip}[a-fA-F\d:.]+)"""
  """exa_json_path=$..NATDestination,exa_regex=({dest_translated_ip}[a-fA-F\d:.]+)"""
  """exa_json_path=$..NATSourcePort,exa_field_name=src_translated_port"""
  """exa_json_path=$..NATDestinationPort,exa_field_name=dest_translated_port"""
  """exa_json_path=$..DirectionOfAttack,exa_field_name=direction"""
  """exa_json_path=$..URL,exa_regex=({malware_url}[^\/"]+)"""
  """exa_regex=(Source)?User(Name)?":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(na|NA|(({domain}[^"\\]+))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$..SourceAddress,exa_field_name=src_ip"""
  """exa_json_path=$..DestinationAddress,exa_field_name=dest_ip"""
  """exa_json_path=$..rule,exa_field_name=rule"""
  """exa_json_path=$..HTTPMethod,exa_field_name=method"""
  """exa_json_path=$..UserAgent,exa_field_name=user_agent"""
  """exa_json_path=$..URLCategory,exa_field_name=category"""
  """exa_regex=(Source)?User(Name)?":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(na|NA|(({domain}[^"\\]+))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$..InboundInterface,exa_field_name=src_interface"""
  """exa_json_path=$..OutboundInterface,exa_field_name=dest_interface"""
  """exa_json_path=$..FromZone,exa_field_name=src_network_zone"""
  """exa_json_path=$..ToZone,exa_field_name=dest_network_zone"""
]
Name = "pan-ngfw-json-alert-trigger-success-threat"
Conditions = [
""""LogType":"THREAT""""
""""VendorSeverity":""""
"""DirectionOfAttack":""""
""""Subtype":"url""""
]
DupFields = [ "malware_url->url" ]
ParserVersion = "v1.0.0"
},

{
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Fields = [
  """exa_json_path=$.event.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.event.DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$..DeviceName,exa_field_name=device_name"""
  """exa_json_path=$.event.PrivateIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PrivateIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PublicIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.LogType,exa_field_name=app"""
  """exa_json_path=$.event.EventStatus,exa_field_name=result"""
  """exa_json_path=$.event.EndpointDeviceName,exa_field_name=src_host"""
  """exa_json_path=$.event.SourceRegion,exa_field_name=src_country"""
  """exa_json_path=$.event.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.event.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=auth_method"""
  """exa_json_path=$.event.SourcePort,exa_field_name=src_port"""
  """exa_json_path=$.event.DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$.event.Protocol,exa_field_name=protocol"""
  """exa_json_path=$.event.EndpointOSVersion,exa_field_name=os"""
  """exa_regex=Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.Description,exa_field_name=additional_info"""
    """exa_json_path=$.event.LogType,exa_field_name=event_category"""
    """exa_json_path=$.event.Action,exa_field_name=action"""
    """exa_regex=({alert_name}spyware)"""
    """exa_json_path=$.event.VendorSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.event.Subtype,exa_field_name=alert_type"""
    """exa_json_path=$.event.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.event.ThreatCategory,exa_regex=((?i:unknown)|({threat_category}[^"]+))"""
    """exa_json_path=$.event.ThreatID,exa_regex=({alert_name}[^"\(]+?)\s*(\(({alert_id}[^"\)]\d+))"""
    """exa_json_path=$.event.Application,exa_field_name=network_app"""
    """exa_json_path=$.event.FileName,exa_regex=({file_name}[^\."]+)*?(\.({file_ext}[^"\.]+))"""
    """exa_json_path=$.event.Rule,exa_field_name=alert_name"""
    """exa_json_path=$.event.SubType,exa_field_name=alert_type"""
    """exa_regex=(Source)?User(Name)?":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(na|NA|(({domain}[^"\\]+))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$..InboundInterface,exa_field_name=src_interface"""
    """exa_json_path=$..OutboundInterface,exa_field_name=dest_interface"""
    """exa_json_path=$..FromZone,exa_field_name=src_network_zone"""
    """exa_json_path=$..ToZone,exa_field_name=dest_network_zone"""
    """exa_json_path=$..NATSource,exa_regex=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$..NATDestination,exa_regex=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
]
Name = "pan-ngfw-json-alert-trigger-success-threatalert"
Conditions = [
""""LogType":"THREAT""""
""""SubType":"file""""
""""Action":"alert""""
]
DupFields = [ "alert_name -> alert_subject" ]
ParserVersion = "v1.0.0"
},

${PaloAltoParsersTemplates.leef-paloalto-vpn-event}{
 Name = pan-gp-leef-vpn-logout-success-globalprotect
 Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """|gateway-logout|""", ]
 ParserVersion = "v1.0.0"
},

${PaloAltoParsersTemplates.paloalto-vpn} {
  Name = pan-ngfw-json-vpn-logout-success-logout
  Product = GlobalProtect
  Conditions = [ """"LogType":"USERID"""", """"DeviceSN":"""", """"Subtype":"logout"""", """"MappingDataSourceType":"globalprotect"""" ]
  Fields = ${PaloAltoParsersTemplates.paloalto-vpn.Fields}[
    """exa_json_path=$.SourceIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"
},

{
    Name = pan-ngfw-kv-network-traffic-success-packetlog
	ParserVersion = v1.0.0
    Vendor = Palo Alto Networks
    Product = Palo Alto NGFW
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """packet_log""", """as_name=""", """as_num=""", """direction=""" ]
    Fields = [
      """packet_log: ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}(-|\+)\d{4})"""
      """\saction=({result}.*?)(,\s\w+=|$)"""
      """\sproto=({protocol}.*?)(,\s\w+=|$)"""
      """\sdirection=({direction}.*?)(,\s\w+=|$)"""
      """\sreason=({result_reason}.*?)(,\s\w+=|$)"""
      """\ssrc=(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))(,\s\w+=|$)"""
      """\sdst=(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))(,\s\w+=|$)"""
      """\ssrc_port=({src_port}\d+)"""
      """\sdst_port=({dest_port}\d+)"""
    
}
```