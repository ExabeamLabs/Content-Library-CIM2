#### Parser Content
```Java
{
Name = vmware-idm-json-app-logout-success-logout
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMWare ID Manager (VIDM)
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
  Conditions = [ """"objectType""", """"vidm""", """"organizationId""", """\"LOGOUT\""""]
  Fields = [
    """"_time":"({time}[^"]+)"""",
    """"host":"({host}[^"]+)"""",
# index is removed
    """"source":"({src_host}[^"]+)"""",
    """"sourcetype":"({domain}[^"]+)"""",
    """"objectType\\*":\s*\\*"({operation}[^\\]+)\\*"""",
    """"objectId\\*":\s*\\*"({object_id}[^\\]+)\\*"""",
    """"objectName\\*":\s*\\*"({target}[^\\]+)\\*"""",
    """"deviceType\\*":\s*\\*"({device_type}[^\\]+)\\*"""",
    """"success\\*":\s*\\*"({result}[^\\]+)\\*"""",
    """"resourceType\\*":\s*\\*"({resource_type}[^\\]+)\\*"""",
    """"deviceId\\*":\s*\\*"({user_agent}[^\\]+)\\*"""",
    """"actorDomain\\*":\s*\\*"({domain}[^\\]+)\\*"""",
    """"actorUserName\\*":\s*\\*"(?:Not Available|({full_name}\w+(?:\s+\w+)+)|({user}[^\\]+))\\*"""",
    """"uuid\\*":\s*\\*"({user_uid}[^\\]+)\\*"""",
    """"actorUuid\\*":\s*\\*"({suid}[^\\]+)\\*"""",
    """"sourceIp\\*":\s*\\*"({src_ip}[^\\]+)\\*"""",
    """"authMethods\\*":\s*\\*"({auth_method}[^\\]+)\\*"""",
    """"redirectUrl\\*":\s*\\*"({redirectUrl}[^\\]+)\\*"""",
    """"failureMessage\\*":\s*\\*"({failure_reason}[^\\]+)\\*"""",
    """"message\\*":\s*\\*"({additional_info}[^\\]+)\\*"""",
    """"event\\*":\s*\\*"({event_name}[^\\]+)\\*"""",
    """"recordAction\\*":\s*\\*"({operation}[^\\]+)\\*"""",
    """"oldValues\\*":\s*\{({old_value}.*?)\}""",
    """"status\\*":\s*\\*"({result}[^\\]+)\\*"""",
    """"recordType\\*":\s*\\*"({object_type}[^\\]+)\\*"""",
    """"osName\\*":\s*\\*"({os}[^\\]+)\\*"""",
    """"osVersion\\*":\s*\\*"({os_version}[^\\]+)\\*"""",
    """"osFamily\\*":\s*\\*"({os_type}[^\\]+)\\*"""",
    """"machineName\\*":\s*\\*"({host}[^\\]+)\\*"""",
    """product=\\*"({app}[^\\"=:]+)\\*"""",
# trigger_event is removed
  ]


}
```