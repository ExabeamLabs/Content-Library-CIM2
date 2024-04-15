#### Parser Content
```Java
{
Name = "vmware-idm-json-app-activity-redirectdenied"
Vendor = "VMware"
Product = "VMware Identity Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [""""objectType""", """vidm""", """"organizationId""", """\"REDIRECT_DENIED\""""]
Fields = [
""""_time":"({time}[^"]+)""""
""""host":"({host}[^"]+)""""
""""source":"({src_host}[^"]+)""""
""""sourcetype":"({domain}[^"]+)""""
""""objectType\\*":\s*\\*"({operation}[^\\]+)\\*""""
""""objectId\\*":\s*\\*"({object_id}[^\\]+)\\*""""
""""objectName\\*":\s*\\*"({target}[^\\]+)\\*""""
""""deviceType\\*":\s*\\*"({device_type}[^\\]+)\\*""""
""""success\\*":\s*\\*"({result}[^\\]+)\\*""""
""""resourceType\\*":\s*\\*"({resource_type}[^\\]+)\\*""""
""""deviceId\\*":\s*\\*"({user_agent}[^\\]+)\\*""""
""""actorDomain\\*":\s*\\*"({domain}[^\\]+)\\*""""
""""actorUserName\\*":\s*\\*"(Not Available|({full_name}\w+(\s+\w+)+)|({user}[^\\]+))\\*""""
""""uuid\\*":\s*\\*"({user_uid}[^\\]+)\\*""""
""""actorUuid\\*":\s*\\*"({suid}[^\\]+)\\*""""
""""sourceIp\\*":\s*\\*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\*""""
""""authMethods\\*":\s*\\*"({auth_method}[^\\]+)\\*""""
""""redirectUrl\\*":\s*\\*"({redirectUrl}[^\\]+)\\*""""
""""failureMessage\\*":\s*\\*"({failure_reason}[^\\]+)\\*""""
""""message\\*":\s*\\*"({additional_info}[^\\]+)\\*""""
""""event\\*":\s*\\*"({event_name}[^\\]+)\\*""""
""""recordAction\\*":\s*\\*"({operation}[^\\]+)\\*""""
""""oldValues\\*":\s*\{({old_value}.*?)\}"""
""""status\\*":\s*\\*"({status}[^\\]+)\\*""""
""""recordType\\*":\s*\\*"({object_type}[^\\]+)\\*""""
""""osName\\*":\s*\\*"({os}[^\\]+)\\*""""
""""osVersion\\*":\s*\\*"({os_version}[^\\]+)\\*""""
""""osFamily\\*":\s*\\*"({os_type}[^\\]+)\\*""""
""""machineName\\*":\s*\\*"({host}[^\\]+)\\*""""
"""product=\\*"({app}[^\\"=:]+)\\*""""
]
ParserVersion = "v1.0.0"


}
```