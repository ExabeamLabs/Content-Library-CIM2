#### Parser Content
```Java
{
Name = jumpcloud-jc-json-directoryinsights-events
  ExtractionType = json
  Vendor = Jumpcloud
  Product = Jumpcloud
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ" ]
  Conditions = [ """"service":""", """"timestamp":""", """"event_type":""", """"organization":""", """"@version":"""  ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.initiated_by.type,exa_field_name=user_type"""
    """exa_json_path=$.initiated_by.username,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
    """exa_json_path=$.geoip.country_code,exa_field_name=country_code"""
    """exa_json_path=$.geoip.region_name,exa_field_name=region"""
    """exa_json_path=$.useragent.os,exa_field_name=os"""
    """exa_json_path=$.useragent.os_version,exa_field_name=os_version"""
    """exa_json_path=$.event_type,exa_field_name=event_category"""
    """exa_json_path=$.service,exa_field_name=resource"""
    """exa_json_path=$.success,exa_field_name=result"""
    """exa_json_path=$.organization,exa_field_name=tenant_id"""
    """exa_json_path=$.client_ip,exa_regex=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(::ffff:)?({=src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?)"""
    """exa_json_path=$.resource.type,exa_field_name=resource_type"""
    """exa_json_path=$.resource.username,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
    """exa_json_path=$.initiated_by.user_id,exa_field_name=user_id"""
    """exa_json_path=$.initiated_by.email,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
    """exa_json_path=$.resource.recipient_email,exa_field_name=dest_email_address"""
    """exa_json_path=$.auth_method,exa_field_name=auth_method"""
    """exa_json_path=$.resource.app_name,exa_field_name=app"""
    """exa_json_path=$.resource.app_id,exa_field_name=app_id"""
    """exa_json_path=$.state,exa_field_name=status_msg"""
    """exa_json_path=$.system.hostname,exa_regex=({host}[\w\-\.]+)"""
    """exa_json_path=$.application.name,exa_field_name=app"""
    """exa_json_path=$.application.version,exa_field_name=app_version"""
    """exa_json_path=$.resource.policy_id,exa_field_name=policy_id"""
    """exa_json_path=$.resource.policy_name,exa_field_name=policy_name"""
    """exa_json_path=$.changes[0].from,exa_field_name=old_value"""
    """exa_json_path=$.changes[0].to,exa_field_name=new_value"""
    """exa_json_path=$.association.op,exa_field_name=operation"""
    """exa_json_path=$.association.connection,exa_field_name=additional_info"""
    """exa_json_path=$.mdm_type,exa_field_name=service_type"""
    """exa_json_path=$.request_type,exa_field_name=command"""
    """exa_json_path=$.mdm_device_id,exa_field_name=device_id"""
    """exa_json_path=$.status,exa_field_name=status_msg"""
    """exa_json_path=$.detail,exa_field_name=more_info"""
    """exa_json_path=$.resource.serial,exa_field_name=device_id"""
    """exa_json_path=$.resource.asset_type,exa_field_name=resource_type"""
    """exa_json_path=$.resource.name,exa_field_name=resource_name"""
    """exa_json_path=$.resource.model,exa_field_name=device_model"""
    """exa_json_path=$.resource.status,exa_field_name=status_msg"""
    """exa_json_path=$.resource.account_email,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
    """exa_json_path=$.resource.application_name,exa_field_name=app"""
    """exa_json_path=$.resource.account_id,exa_field_name=account_id"""
    """exa_json_path=$.resource.discovery_info.browser_type,exa_field_name=browser"""
    """exa_json_path=$.resource.login_type,exa_field_name=login_type_text"""
    """exa_json_path=$.resource.user_id,exa_field_name=user_id"""
    """exa_json_path=$.resource.account_identifier,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
    """exa_json_path=$.referrer_type,exa_field_name=referrer"""
    """exa_json_path=$.object_storage_item_version_sha_256_sum,exa_field_name=hash_sha256"""
    """exa_json_path=$.object_storage_item_version_name,exa_field_name=object_name"""
    """exa_json_path=$.object_storage_item_version_size,exa_field_name=bytes"""
    """exa_json_path=$.initiated_by.username,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
     """exa_json_path=$.initiated_by[?(@.type == 'user')].username,exa_field_name=user"""
     """exa_json_path=$.geoip.country_code,exa_field_name=country_code"""
     """exa_json_path=$.geoip.city,exa_field_name=location_city"""
     """exa_json_path=$.geoip.region_name,exa_field_name=region"""
     """exa_json_path=$.error_message,exa_field_name=failure_reason""",
     """exa_json_path=$.message,exa_field_name=additional_info""",
     """exa_json_path=$.system.hostname,exa_regex=({host}[\w\-\.]+)"""
     """exa_json_path=$.event_type,exa_field_name=event_name""",
     """exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """exa_json_path=$.username,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
     """exa_json_path=$.process_name,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""
     """exa_json_path=$.useragent.os,exa_field_name=user_agent_client""",
      """exa_json_path=$.useragent.os_full,exa_field_name=os_version""",
      """exa_json_path=$.useragent.device,exa_field_name=device_type""",
     """exa_json_path=$.event_type,exa_field_name=event_name""",
     """exa_json_path=$.mfa_meta.type,exa_field_name=auth_type""",
     """exa_json_path=$.auth_context.policies_applied[0].metadata.resource_type,exa_field_name=resource_type""",
    """exa_json_path=$.auth_context.policies_applied[0].metadata.action,exa_field_name=action""",
    """exa_json_path=$.auth_context.policies_applied[0].name,exa_field_name=policy_name""",
     """exa_json_path=$.mfa,exa_field_name=mfa"""
     """"username":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """error_message":"({failure_reason}[^",]+)""""
    """"country_code":"({country_code}[^"]+)""""
    """"region_name":"({region}[^"]+)""""
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
    """"event_type":"({event_name}[^"]+)""""
    """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"mfa":({mfa}[^",]+)"""
    """"os_name":"({os}[^"]+)""""
    """"os_version":"({os_version}[^"]+)""""
    ]
    ParserVersion = "v1.0.0"


}
```