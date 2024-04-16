#### Parser Content
```Java
{
Name = "sailpoint-identitynow-json-app-activity-success-usermanagement"
Vendor = "Sailpoint"
Product = "IdentityNow"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""type": "USER_MANAGEMENT""""
""""stack": """"
""""attributes":"""
]
Fields = [
"""exa_json_path=$.created,exa_field_name=time""",
"""exa_json_path=$.action,exa_field_name=operation""",
"""exa_json_path=$.attributes.hostName,exa_regex=(\d+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^",]+))""",
"""exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.type,exa_regex=((?i:NONE|null)|({operation_type}[^"]+))""",
"""exa_json_path=$.technicalName,exa_field_name=event_name""",
"""exa_json_path=$.actor.name,exa_regex=(?i:Not Available|unknown|({full_name}[^\s",]+(|,)\s[^\s",]+)|({user}[\w\.\-]{1,40}\$?))$""",
"""exa_json_path=$.attributes.sourceName,exa_regex=((?i:null|NONE)|({app}[^"]+))""",
"""exa_json_path=$.attributes.info,exa_regex=((?i:null|NONE)|({additional_info}[^"]+))"""
"""exa_json_path=$.status,exa_regex=((?i:null|NONE)|({result}[^"]+))$"""
]
ParserVersion = "v1.0.0"


}
```