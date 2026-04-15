#### Parser Content
```Java
{
Name = jumpcloud-jc-str-app-login-success
   Vendor = Jumpcloud
   Product = Jumpcloud
   ParserVersion = "v1.0.0"
   TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" , "yyyy-MM-dd'T'HH:mm:ss.SSSZ" , "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
   ExtractionType = json
   Conditions = [ """User """, """ logged in """, """, process name: """, """, time: """ ]
   Fields = [
     """time:\s+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{1,7}Z)""",
     """User\s+(-|(({email_address}[^@"]+@({email_domain}[^\.]+\.[^"]+?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^~"]+?)))\s+({event_name}logged in)""",
     """process name:\s+(-|({process_path}[^,]+?)),\s""",
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
     """exa_json_path=$.timestamp,exa_field_name=time"""
     """exa_json_path=$.useragent.os,exa_field_name=user_agent_client""",
      """exa_json_path=$.useragent.os_full,exa_field_name=os_version""",
      """exa_json_path=$.useragent.device,exa_field_name=device_type""",
     """exa_json_path=$.mfa_meta.type,exa_field_name=auth_type""",
     """exa_json_path=$.auth_context.policies_applied[0].metadata.resource_type,exa_field_name=resource_type""",
    """exa_json_path=$.auth_context.policies_applied[0].metadata.action,exa_field_name=action""",
    """exa_json_path=$.auth_context.policies_applied[0].name,exa_field_name=policy_name""",
     """exa_json_path=$.mfa,exa_field_name=mfa""",
   ]


}
```