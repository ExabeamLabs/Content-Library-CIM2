#### Parser Content
```Java
{
Name = "cisco-fp-json-alert-trigger-success-connectiontimestamp"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "epoch_sec"
Conditions = [
  """"connectionTimestamp":"""
  """"applicationProtocol":"""
  """"securityZoneEgressUuid":"""
]
Fields = [
  """"connectionTimestamp":\s*({time}\d{10})"""
  """"sensor":\s*"({host}[^"]+?)""""
  """"sensor":\s*"[^"]+?\s+-\s+({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
  """"sourcePortOrIcmpType":\s*({src_port}\d+)"""
  """"eventId":\s*({alert_id}[^",]+)"""
  """"message":\s*"({additional_info}[^"]+)"""
  """"recordTypeDescription":\s*"({alert_name}[^"]+)"""
  """"priority":\s*"({alert_severity}[^"]+)"""
  """"user":\s*"(?:Unknown|No Authentication Required|({user}[^"]+))"""
  """"destinationPortOrIcmpType":\s*({dest_port}\d+)"""
  """"transportProtocol":\s*"({protocol}[^"]+)"""
  """"sourceIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"destinationIpAddress":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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
  """"blocked":\s*({blocked}[^",]+)"""
  """"connectionCounter":\s*({connection_counter}[^",]+)"""
  """"ipProtocolId":\s*({ip_protocol_id}[^",]+)"""
  """"destinationCountry":\s*({dest_country}[^",]+)"""
  """"ingressSecurityZone":\s*"(N\/A|({ingressSecurity_zone}[^"]+))"""
  """"ingressInterface":\s*"(N\/A|({ingress_interface}[^"]+))"""
  """"egressSecurityZone":\s*"(N\/A|({egress_security_zone}[^"]+))"""
  """"impactDescription":\s*"({impact}[^"]+)"""
  """"classificationName":\s*"({classification_name}[^"]+)"""
  """"blockType":\s*({block_type}[^",]+)"""
  """"deviceId":\s*({device_id}[^",\}]+)"""
  """"transportProtocol":\s*"({protocol}[^"]+)"""
  """"userId":\s*({user_id}\d+)"""
  """"firewallPolicy":\s*"({src_country}[^"]+)"""
  """"blocked":\s*"({blocked}[^"]+?)""""
  """({result}"blocked":\s*"(Yes|No)")"""
]
DupFields = [
  "host->sensor"
  "classification_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```