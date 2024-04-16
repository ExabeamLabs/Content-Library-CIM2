#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-anonymouslogin
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
  """"vendor": "Microsoft""""
  """"riskScore":"""
  """"malwareStates":"""
]
Fields = [
  """exa_json_path=$.userStates..userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.userStates..logonIp,exa_field_name=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.userStates..accountName,exa_field_name=user"""
  """exa_json_path=$.userStates..domainName,exa_field_name=domain"""
  """exa_json_path=$.createdDateTime,exa_field_name=time"""
  """exa_json_path=$.severity,exa_field_name=alert_severity"""
  """exa_json_path=$.id,exa_field_name=alert_id"""
  """exa_json_path=$.description,exa_field_name=additional_info"""
  """exa_json_path=$.category,exa_field_name=alert_name"""
  """exa_json_path=$.category,exa_field_name=alert_type"""
  """exa_json_path=$.title,exa_field_name=alert_name"""
  """exa_json_path=$.status,exa_field_name=result"""
  """exa_json_path=$.userStates..logonLocation,exa_field_name=location"""
]
ParserVersion = "v1.0.0"


}
```