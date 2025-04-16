#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-app-notification-success-catchall
  ParserVersion = v1.0.0
  Conditions = [ """"primaryDescription":""", """"activityType":""", """"activityUuid":""", """"threatId":""" ]

json-sentinelone-activitytype = {
  Vendor = SentinelOne
  Product = "Singularity Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Fields = [
  """exa_json_path=$.createdAt,exa_field_name=time""",
  """exa_json_path=$..computerName,exa_field_name=src_host""",
  """exa_json_path=$..ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$..confidenceLevel,exa_field_name=additional_info""",
  """exa_json_path=$.accountName,exa_field_name=account_name"""
  """exa_json_path=$..filePath,exa_field_name=file_path""" 
  """exa_json_path=$..fileDisplayName,exa_field_name=file_name""" 
  """exa_json_path=$.groupName,exa_field_name=group_name""",
  """exa_json_path=$..fileContentHash,exa_regex=^(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))$""",
  """exa_json_path=$.accountId,exa_field_name=account_id""",
  """exa_json_path=$.activityType,exa_field_name=event_code""",
  """exa_json_path=$.threatId,exa_field_name=alert_id""",
  """exa_json_path=$..email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))$""",
  """exa_json_path=$..username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
  """exa_json_path=$..userName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
  """exa_json_path=$.primaryDescription,exa_field_name=additional_info""",
  """exa_json_path=$..osType,exa_field_name=os"""
  
}
```