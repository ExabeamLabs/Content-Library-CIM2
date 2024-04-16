#### Parser Content
```Java
{
Name = "workday-wd-json-app-activity-success-activityaction"
Vendor = "Workday"
Product = "Workday"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""activityAction":"""
""""tenantHost":"""
"""workday"""
]
Fields = [
"""exa_json_path=$.userAgent,exa_field_name=user_agent"""
"""exa_json_path=$.requestTime,exa_field_name=time"""
"""exa_json_path=$.deviceType,exa_field_name=device_type"""
"""exa_json_path=$.systemAccount,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
"""exa_json_path=$.tenantHost,exa_field_name=host"""
"""exa_json_path=$.activityAction,exa_field_name=additional_info"""
"""exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.target.descriptor,exa_field_name=object"""
"""exa_json_path=$.taskDisplayName,exa_field_name=operation"""
"""exa_regex=({app}(W|w)orkday)"""
]
ParserVersion = "v1.0.0"


}
```