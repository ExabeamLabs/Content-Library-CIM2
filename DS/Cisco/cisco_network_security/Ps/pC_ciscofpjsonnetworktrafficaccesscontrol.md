#### Parser Content
```Java
{
Name = "cisco-fp-json-network-traffic-accesscontrol"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """"protocol":"""
    """"recordType": 71,"""
    """"eventType":"""
    """"recordTypeDescription":"""
  ]
  Fields = [
    """exa_json_path=$.@computed.eventDateTime,exa_field_name=time"""
    """exa_json_path=$.@computed.sensor,exa_field_name=host"""
    """exa_json_path=$.@computed.firewallRuleAction,exa_field_name=action"""
    """exa_json_path=$.@computed.firewallRule,exa_field_name=rule"""
    """exa_json_path=$.initiatorIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.responderIpAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.responderPort,exa_field_name=dest_port"""
    """exa_json_path=$.@computed.clientApplication,exa_field_name=network_app"""
    """exa_json_path=$.@computed.transportProtocol,exa_field_name=protocol"""
    """exa_json_path=$.initiatorTransmittedBytes,exa_field_name=bytes_out"""
    """exa_json_path=$.responderTransmittedPackets,exa_field_name=bytes_in"""
    """exa_json_path=$.@computed.ingressInterface,exa_field_name=src_interface"""
    """exa_json_path=$.@computed.egressInterface,exa_field_name=dest_interface"""
    """exa_json_path=$.@computed.user,exa_regex=(No Authentication Required|(?i)Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.@computed.recordTypeDescription,exa_field_name=event_name"""
    """exa_json_path=$.clientUrl.data,exa_field_name=additional_info"""
    """exa_json_path=$.initiatorPort,exa_field_name=src_port"""
  ]


}
```