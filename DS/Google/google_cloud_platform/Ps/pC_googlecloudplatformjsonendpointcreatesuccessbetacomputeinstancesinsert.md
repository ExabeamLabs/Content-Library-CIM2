#### Parser Content
```Java
{
Name = google-cloudplatform-json-endpoint-create-success-betacomputeinstancesinsert
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """googleapis.com""", """"methodName":""", """compute.instances.insert"""" ]
  Fields = ${GcpParserTemplates.gcp-cloudaudit-json.Fields}[
    """exa_regex="timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_regex="source({src_resource_type}Snapshot)":\s*"({src_resource}[^"\\]+)"""",
    """exa_regex="source({src_resource_type}Image)":\s*"({src_resource}[^"\\]+)"""",
    """exa_regex="source({src_resource_type}Disk)":\s*"({src_resource}[^"\\]+)"""",
    """exa_json_path=$.protoPayload.request.machineType,exa_field_name=machine_type""",
    """exa_json_path=$.protoPayload.request.serviceAccounts[:1].email,exa_field_name=linked_service_account""",
    """exa_json_path=$.protoPayload.request.networkInterfaces[:1].subnetwork,exa_field_name=subnetwork""",
  ]
  DupFields = ["src_resource->source_resource", "src_resource_type->source_resource_type"]

gcp-cloudaudit-json = {
    Vendor = Google
    Product = Google Cloud Platform
    ExtractionType = json
    TimeFormat = ["epoch","MM.dd.yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss"]
    Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"logName"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"log-name"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"status":.+"code":\s*({result_code}\d+)""",
    """"status":.+"message":\s*({failure_reason}[^\\},]+)""",
    """"principalEmail":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"callerIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"callerSuppliedUserAgent":\s*"({user_agent}[^"]+)""",
    """"methodName":\s*"({operation}[^"]+)""",
    """"resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))"""",
    """"serviceName":\s*"({service_name}[^"]+)""",
    """"resource":\s*\{\s*"type":\s*"({resource_type}[^"\\\/]+)"""",
    """"resource"+:[^\}]*labels[^\}]*"+project_id"+:\s*"+({project_id}[^"\\\/\}]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+zone"+:\s*"+({zone}[^"\\\/\}]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+location"+:\s*"+({region}[^"\\\/\}]+)"+""",
    """"resource"+:[^\}]*labels[^\}]*"+bucket_name"+:\s*"+({bucket_name}[^"\\\/\}]+)"+""",
    """"operation"+:[^\}]*first"+:\s*({operation_first}[^"\\\/\}\s,]+)""",
    """"operation"+:[^\}]*last"+:\s*({operation_last}[^"\\\/\}\s,]+)""",
    """"severity":"({severity}[^"]+)""",
    """etag":"({tag}[^"]+)""",
    """"(response|request)"+:.+"+bindings"+:\s*\[\s*({policy_bindings}.+)\s*\],?[\s\]\},]+(?:"+resourceLocation"+|"+resource"+|"+@type"+|"+etag"+|"+version"+|"+serviceName"+)""",
    """"authorizationInfo":\[\{[^\}]+"permissionType":"({operation_type}[^"]+)""",
    """"authorizationInfo":\[\{[^\}]+"permission":"({permission}[^"]+)""",
    """exa_json_path=$..logEntries..timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.logName,exa_field_name=event_category""",
    """exa_json_path=$.log-name,exa_field_name=event_category""",
    """exa_json_path=$..status.code,exa_field_name=result_code""",
    """exa_json_path=$..status.message,exa_field_name=failure_reason""",
    """exa_json_path=$..authenticationInfo.serviceAccountDelegationInfo[:1].firstPartyPrincipal.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..authenticationInfo.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..access.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..requestMetadata.callerIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..access.callerIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_json_path=$..requestMetadata.callerSuppliedUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$..access.userAgent,exa_field_name=user_agent""",
    """exa_json_path=$..methodName,exa_field_name=operation""",
    """exa_json_path=$..access.methodName,exa_field_name=operation""",
    """exa_json_path=$..resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))""",
    """exa_json_path=$..resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))""",
    """exa_json_path=$..serviceName,exa_field_name=service_name""",
    """exa_json_path=$..access.serviceName,exa_field_name=service_name""",
    """exa_json_path=$.resource.type,exa_field_name=resource_type""",
    """exa_json_path=$.resource.labels.project_id,exa_field_name=project_id""",
    """exa_json_path=$.resource.labels.zone,exa_field_name=zone""",
    """exa_json_path=$.resource.labels.location,exa_field_name=region""",
    """exa_json_path=$.resource.labels.bucket_name,exa_field_name=bucket_name,exa_match_expr=!InList($.resource.labels.bucket_name,"")""",
    """exa_json_path=$.operation.first,exa_field_name=operation_first""",
    """exa_json_path=$.operation.last,exa_field_name=operation_last"""
    """exa_json_path=$..request.storageLocations[0],exa_field_name=location""",
    """exa_json_path=$..response.operationType,exa_field_name=operation_type"""
    """exa_json_path=$.protoPayload.request.policy.etag,exa_field_name=tag"""
    """exa_json_path=$.severity,exa_field_name=severity"""
    """exa_json_path=$.protoPayload.authorizationInfo[:1].permission,exa_field_name=permission"""
    """exa_json_path=$.protoPayload.authorizationInfo[:1].permissionType,exa_field_name=operation_type"""
    
}
```