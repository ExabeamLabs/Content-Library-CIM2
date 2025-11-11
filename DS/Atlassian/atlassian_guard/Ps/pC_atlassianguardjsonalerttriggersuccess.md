#### Parser Content
```Java
{
Name = "atlassian-guard-json-alert-trigger-success"
  Vendor = "Atlassian"
  Product = "Atlassian Guard"
  TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  start_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  end_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """"alertDetailURL":""", """detect.atlassian.com""", """"alertId":""", """"alertTitle":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.alertDetailURL,exa_field_name=url"""
     """exa_json_path=$.alertId,exa_field_name=alert_id"""
     """exa_json_path=$.alertTitle,exa_field_name=alert_name"""
     """exa_json_path=$.activity.action,exa_field_name=action"""
     """exa_json_path=$.activity.time.start,exa_field_name=start_time"""
     """exa_json_path=$.activity.time.end,exa_field_name=end_time"""
     """exa_json_path=$.actor.accountId,exa_field_name=account_id"""
     """exa_json_path=$.actor.name,exa_field_name=full_name"""
     """exa_json_path=$.actor.sessions[0].ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """exa_json_path=$.actor.sessions[0].userAgent,exa_field_name=user_agent"""
     """exa_json_path=$.type,exa_field_name=operation"""
     """exa_json_path=$.activity.subject.resourceName,exa_field_name=resource_name"""
     """exa_json_path=$.alert.product,exa_field_name=product_name"""
  ]


}
```