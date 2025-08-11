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
""""systemAccount":"""
""""taskDisplayName":"""
]
Fields = [
"""exa_json_path=$.userAgent,exa_field_name=user_agent"""
"""exa_json_path=$.requestTime,exa_field_name=time"""
"""exa_json_path=$.deviceType,exa_field_name=device_type"""
"""exa_json_path=$.systemAccount,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$"""
"""exa_json_path=$.tenantHost,exa_field_name=host"""
"""exa_json_path=$.activityAction,exa_field_name=additional_info"""
"""exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.target.descriptor,exa_field_name=object"""
"""exa_json_path=$.taskDisplayName,exa_field_name=operation"""
"""exa_json_path=$.sessionId,exa_field_name=session_id""",
"""exa_json_path=$.taskId,exa_field_name=task_id""",
"""exa_regex=({app}(W|w)orkday)"""
""""userAgent":"({user_agent}[^"]+)"""
""""requestTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""deviceType":"({device_type}[^"]+)"""
""""systemAccount":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""({app}(W|w)orkday)"""
""""activityAction":"({additional_info}[^"]+)"""
""""taskDisplayName":"({operation}[^"]+)"""
""""ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""sessionId":"({session_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```