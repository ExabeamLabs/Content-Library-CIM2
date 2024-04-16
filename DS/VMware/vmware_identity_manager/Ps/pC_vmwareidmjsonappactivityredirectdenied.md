#### Parser Content
```Java
{
Name = "vmware-idm-json-app-activity-redirectdenied"
Vendor = "VMware"
Product = "VMware Identity Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
ExtractionType = json
Conditions = [""""objectType""", """vidm""", """"organizationId""", """\"REDIRECT_DENIED\""""]
Fields = [
"""exa_json_path=$.result._time,exa_field_name=time"""
"""exa_json_path=$.result.host,exa_regex=^({host}[\w\-.]+?)(:\d+)?$"""
"""exa_json_path=$.result.source,exa_regex=^(\w+:)?({src_host}[\w\-.]+?)$"""
"""exa_json_path=$.result.sourcetype,exa_field_name=domain"""
"""exa_json_path=$.result._raw,exa_regex=objectType\\*":\s*\\*"({operation}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=objectId\\*":\s*\\*"({object_id}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=objectName\\*":\s*\\*"({target}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=deviceType\\*":\s*\\*"({device_type}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=success\\*":\s*\\*"({result}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=deviceId\\*":\s*\\*"({user_agent}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=actorDomain\\*":\s*\\*"({domain}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=actorUserName\\*":\s*\\*"(Not Available|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-]{1,40}\$?))\\*"""
"""exa_json_path=$.result._raw,exa_regex=uuid\\*":\s*\\*"({user_uid}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=actorUuid\\*":\s*\\*"({suid}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=sourceIp\\*":\s*\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\*"""
"""exa_json_path=$.result._raw,exa_regex=authMethods\\*":\s*\\*"({auth_method}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=redirectUrl\\*":\s*\\*"({redirectUrl}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=failureMessage\\*":\s*\\*"({failure_reason}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=message\\*":\s*\\*"({additional_info}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=event\\*":\s*\\*"({event_name}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=recordAction\\*":\s*\\*"({operation}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=oldValues\\*":\s*\{({old_value}.*?)\}"""
"""exa_json_path=$.result._raw,exa_regex=rstatus\\*":\s*\\*"({status}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=recordType\\*":\s*\\*"({object_type}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=osName\\*":\s*\\*"({os}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=osVersion\\*":\s*\\*"({os_version}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=osFamily\\*":\s*\\*"({os_type}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=machineName\\*":\s*\\*"({host}[^\\"]+)\\*"""
"""exa_json_path=$.result._raw,exa_regex=product=\\*"({app}[^\\"=:]+)\\*"""
]
ParserVersion = "v1.0.0"


}
```