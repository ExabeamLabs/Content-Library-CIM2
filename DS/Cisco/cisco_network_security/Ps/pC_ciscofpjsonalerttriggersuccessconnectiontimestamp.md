#### Parser Content
```Java
{
Name = "cisco-fp-json-alert-trigger-success-connectiontimestamp"
Vendor = "Cisco"
Product = Cisco Network Security
ExtractionType = json
TimeFormat = "epoch_sec"
Conditions = [
  """"connectionTimestamp":"""
  """"applicationProtocol":"""
  """"securityZoneEgressUuid":"""
]
Fields = [
  """"connectionTimestamp":\s*({time}\d{10})"""
  """"sensor":\s*"({sensor}({host}[^"]+?))""""
  """"sensor":\s*"[^"]+?\s+-\s+({sensor}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """"sourcePortOrIcmpType":\s*({src_port}\d+)"""
  """"eventId":\s*({alert_id}[^",]+)"""
  """"message":\s*"({additional_info}[^"]+)"""
  """"recordTypeDescription":\s*"({alert_name}[^"]+)"""
  """"priority":\s*"({alert_severity}[^"]+)"""
  """"user":\s*"(?:Unknown|No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"destinationPortOrIcmpType":\s*({dest_port}\d+)"""
  """"transportProtocol":\s*"({protocol}[^"]+)"""
  """"sourceIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"destinationIpAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"applicationProtocol":\s*"(Unknown|({app_protocol}[^"]+))"""
  """"classificationDescription":\s*"({alert_description}[^"]+)"""
  """"clientApplication":\s*"(Unknown|({process_name}[^"]+))"""
  """"idsPolicy":\s*"({policy_name}[^"]+)"""
  """"ruleId":\s*({rule_id}[^",]+)"""
  """"blockLength":\s*({bytes}\d+)"""
  """"recordType":\s*({record_type}[^",]+)"""
  """"iocNumber":\s*({ioc_number}[^",]+)"""
  """"sourceCountry":\s*({src_country}[^",]+)"""
  """"applicationId":\s*({app_id}[^",]+)"""
  """"blocked":\s*({result}({blocked}[^",]+))"""
  """"connectionCounter":\s*({connection_counter}[^",]+)"""
  """"ipProtocolId":\s*({ip_protocol_id}[^",]+)"""
  """"destinationCountry":\s*({dest_country}[^",]+)"""
  """"ingressSecurityZone":\s*"(N\/A|({ingress_zone}[^"]+))"""
  """"ingressInterface":\s*"(N\/A|({ingress_interface}[^"]+))"""
  """"egressSecurityZone":\s*"(N\/A|({egress_security_zone}[^"]+))"""
  """"impactDescription":\s*"({impact}[^"]+)"""
  """"classificationName":\s*"({alert_type}({classification_name}[^"]+))"""
  """"blockType":\s*({block_type}[^",]+)"""
  """"deviceId":\s*({device_id}[^",\}]+)"""
  """"transportProtocol":\s*"({protocol}[^"]+)"""
  """"userId":\s*({user_id}\d+)"""
  """"firewallPolicy":\s*"({src_country}[^"]+)"""
  """"blocked":\s*"({result}({blocked}[^"]+?))""""
  """exa_json_path=$.connectionTimestamp,exa_field_name=time""",
  """exa_json_path=$.@computed.sensor,exa_field_name=host""",
  """exa_json_path=$.@computed.sensor,exa_field_name=sensor""",
  """exa_json_path=$.@computed.sensor,exa_regex=[^"]+?\s+-\s({sensor}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
  """exa_json_path=$.sourcePortOrIcmpType,exa_field_name=src_port""",
  """exa_json_path=$.eventId,exa_field_name=alert_id""",
  """exa_json_path=$.@computed.message,exa_field_name=additional_info""",
  """exa_json_path=$.@computed.recordTypeDescription,exa_field_name=alert_name""",
  """exa_json_path=$.@computed.priority,exa_field_name=alert_severity""",
  """exa_json_path=$.@computed.user,exa_regex=(?:Unknown|No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """exa_json_path=$.destinationPortOrIcmpType,exa_field_name=dest_port""",
  """exa_json_path=$.@computed.transportProtocol,exa_field_name=protocol""",
  """exa_json_path=$.sourceIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.destinationIpAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_regex="applicationProtocol":\s*"(Unknown|({app_protocol}[^"]+))""",
  """exa_json_path=$.@computed.classificationDescription,exa_field_name=alert_description""",
  """exa_regex="clientApplication":\s*"(Unknown|({process_name}[^"]+))""",
  """exa_json_path=$.@computed.idsPolicy,exa_field_name=policy_name""",
  """exa_json_path=$.ruleId,exa_field_name=rule_id""",
  """exa_json_path=$.blockLength,exa_field_name=bytes""",
  """exa_json_path=$.recordType,exa_field_name=record_type""",
  """exa_json_path=$.iocNumber,exa_field_name=ioc_number""",
  """exa_json_path=$.sourceCountry,exa_field_name=src_country""",
  """exa_json_path=$.applicationId,exa_field_name=app_id""",
  """exa_json_path=$.blocked,exa_field_name=blocked""",
  """exa_json_path=$.blocked,exa_field_name=result""",
  """exa_json_path=$.connectionCounter,exa_field_name=connection_counter""",
  """exa_json_path=$.ipProtocolId,exa_field_name=ip_protocol_id""",
  """exa_json_path=$.destinationCountry,exa_field_name=dest_country""",
  """exa_regex="ingressSecurityZone":\s*"(N\/A|({ingress_zone}[^"]+))""",
  """exa_regex="ingressInterface":\s*"(N\/A|({ingress_interface}[^"]+))""",
  """exa_regex="egressSecurityZone":\s*"(N\/A|({egress_security_zone}[^"]+))""",
  """exa_json_path=$.@computed.impactDescription,exa_field_name=impact""",
  """exa_json_path=$.@computed.classificationName,exa_field_name=classification_name""",
  """exa_json_path=$.@computed.classificationName,exa_field_name=alert_type""",
  """exa_json_path=$.blockType,exa_field_name=block_type""",
  """exa_json_path=$.deviceId,exa_field_name=device_id""",
  """exa_json_path=$.@computed.transportProtocol,exa_field_name=protocol""",
  """exa_json_path=$.userId,exa_field_name=user_id""",
  """exa_json_path=$.@computed.firewallPolicy,exa_field_name=src_country""",
  """exa_json_path=$.@computed.blocked,exa_field_name=blocked"""
  """exa_json_path=$.@computed.blocked,exa_field_name=result"""
]
ParserVersion = "v1.0.0"


}
```