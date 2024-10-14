#### Parser Content
```Java
{
Name = google-cloudplatform-json-policy-modify-success-computeimagessetiampolicy
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  ParserVersion = "v1.0.0"
  Conditions = [ """googleapis.com""", """"methodName":""", """compute.images.setIamPolicy"""" ]
  Fields = ${GcpParserTemplates.gcp-cloudaudit-json.Fields}[
    """exa_regex="policy"+:[^\}]+"+bindings"+:\s*\[\s*({policy_bindings}.+)\s*\],?[\s\]\},]+(?:"+resourceLocation"+|"+resource"+|"+@type"+|"+etag"+|"+version"+)""",
  ]

gcp-cloudaudit-json = {
    Vendor = Google
    Product = Google Cloud Platform
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
    Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3,9}Z)""",
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3,9}Z)""",
    """"logName"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"log-name"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"status":.+"code":\s*({result_code}\d+)""",
    """"status":.+"message":\s*({failure_reason}[^\\},]+)""",
    """"principalEmail":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"callerIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"callerSuppliedUserAgent":\s*"({user_agent}[^"]+)""",
    """"methodName":\s*"({operation}[^"]+)""",
    """"resourceName":\s*"({resource}({resource_path}[^"]+)\/({resource_name}[^"\/]+))"""",
    """"serviceName":\s*"({service_name}[^"]+)""",
    """"resource":\s*\{\s*"type":\s*"({resource_type}[^"\\\/]+)"""",
    """"resource"+:[^\}]*labels[^\}]*"+project_id"+:\s*"+({project_id}[^"\\\/\}]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+zone"+:\s*"+({zone}[^"\\\/\}]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+location"+:\s*"+({region}[^"\\\/\}]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+bucket_name"+:\s*"+({bucket_name}[^"\\\/\}]+)"+""",
    """"operation"+:[^\}]*first"+:\s*({operation_first}[^"\\\/\}\s,]+)""",
    """"operation"+:[^\}]*last"+:\s*({operation_last}[^"\\\/\}\s,]+)""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.logName,exa_field_name=event_category""",
    """exa_json_path=$.log-name,exa_field_name=event_category""",
    """exa_json_path=$.protoPayload.status.code,exa_field_name=result_code""",
    """exa_json_path=$.protoPayload.status.message,exa_field_name=failure_reason""",
    """exa_json_path=$.protoPayload.authenticationInfo.serviceAccountDelegationInfo[:1].firstPartyPrincipal.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.protoPayload.authenticationInfo.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.jsonPayload.access.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.protoPayload.requestMetadata.callerIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.jsonPayload.access.callerIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_json_path=$.protoPayload.requestMetadata.callerSuppliedUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.jsonPayload.access.userAgent,exa_field_name=user_agent""",
    """exa_json_path=$.protoPayload.methodName,exa_field_name=operation""",
    """exa_json_path=$.jsonPayload.access.methodName,exa_field_name=operation""",
    """exa_json_path=$.jsonPayload.resourceName,exa_regex=({resource}({resource_path}[^"]+)\/({resource_name}[^"\/]+))""",
    """exa_json_path=$.protoPayload.resourceName,exa_regex=({resource}({resource_path}[^"]+)\/({resource_name}[^"\/]+))""",
    """exa_json_path=$.protoPayload.serviceName,exa_field_name=service_name""",
    """exa_json_path=$.jsonPayload.access.serviceName,exa_field_name=service_name""",
    """exa_json_path=$.resource.type,exa_field_name=resource_type""",
    """exa_json_path=$.resource.labels.project_id,exa_field_name=project_id""",
    """exa_json_path=$.resource.labels.zone,exa_field_name=zone""",
    """exa_json_path=$.resource.labels.location,exa_field_name=region""",
    """exa_json_path=$.resource.labels.bucket_name,exa_field_name=bucket_name,exa_match_expr=!InList($.resource.labels.bucket_name,"")""",
    """exa_json_path=$.operation.first,exa_field_name=operation_first""",
    """exa_json_path=$.operation.last,exa_field_name=operation_last"""
    """exa_json_path=$.protoPayload.request.storageLocations[0],exa_field_name=location""",
    """exa_json_path=$.protoPayload.response.operationType,exa_field_name=operation_type"""
    
}
```