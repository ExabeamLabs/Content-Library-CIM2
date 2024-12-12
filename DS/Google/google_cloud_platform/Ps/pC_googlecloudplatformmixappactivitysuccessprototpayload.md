#### Parser Content
```Java
{
Name = google-cloudplatform-mix-app-activity-success-prototpayload
  Vendor = Google
  Product = Google Cloud Platform
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """"protoPayload":""", """googleapis.com""", """"resourceName":""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{3,9}Z)""",
    """"callerIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"serviceName":"({service_name}[^"]+)"""",
    """"callerSuppliedUserAgent":\s*"({user_agent}[^"]+)""",
    """"principalEmail":\s*"(?:({email_address}[^"@]+?@({email_domain}[^"@]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"methodName":\s*"({operation}[^"]+)""",
    """"serviceName":\s*"({app}[^"]+)""",
    """\sdproc=({app}[^=]+)\s\w+=""",
    """"bucket_name":"({bucket_name}[^",}]+)""""
    """"resource":\s*\{\s*"type":\s*"({resource_type}[^"\\\/]+)"""",
    """"resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))"""",
    """"resource"+:[^\}]*labels[^\}]*"+location"+:\s*"+({region}[^"\\\/\}]+)"+""",
    """"operation"+:[^\}]*first"+:\s*({operation_first}[^"\\\/\}\s,]+)""",
    """"operation"+:[^\}]*last"+:\s*({operation_last}[^"\\\/\}\s,]+)""",
    """"logName"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"log-name"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+project_id"+:\s*"+({project_id}[^"\\\/\}]+)"+"""
    """"status":.+"code":\s*({result_code}\d+)""",
    """"status":.+"message":\s*"?({failure_reason}[^},]+)"""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.protoPayload.requestMetadata.callerIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="callerIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_json_path=$.protoPayload.serviceName,exa_field_name=service_name""",
    """exa_json_path=$.protoPayload.requestMetadata.callerSuppliedUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.protoPayload.authenticationInfo.principalEmail,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.protoPayload.methodName,exa_field_name=operation""",
    """exa_json_path=$.protoPayload.serviceName,exa_field_name=app""",
    """exa_json_path=$.resource.labels.bucket_name,exa_field_name=bucket_name""",
    """exa_json_path=$.resource.type,exa_field_name=resource_type""",
    """exa_json_path=$.resource.labels.location,exa_field_name=region""",
    """exa_json_path=$.protoPayload.resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))""",
    """exa_regex=\sdproc=({app}[^=]+)\s\w+=""",
    """exa_json_path=$.operation.first,exa_field_name=operation_first""",
    """exa_json_path=$.operation.last,exa_field_name=operation_last""",
    """exa_json_path=$.logName,exa_field_name=event_category""",
    """exa_json_path=$.log-name,exa_field_name=event_category""",
    """exa_json_path=$.resource.labels.project_id,exa_field_name=project_id""",
    """exa_json_path=$.protoPayload.status.code,exa_field_name=result_code""",
    """exa_json_path=$.protoPayload.status.message,exa_field_name=failure_reason"""
  ]


}
```