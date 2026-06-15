#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-login-apiactivityauditevent
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = ["epoch_sec", "epoch", "yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"eventType":""", """"OperationName":""", """APIActivityAuditEvent""" ]
  Fields = [
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_json_path=$..UTCTimestamp,exa_field_name=time""",
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$.event.SessionId,exa_field_name=session_id""",
    """exa_json_path=$..UserId,exa_regex=(({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.event.UserName,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$..UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$..ServiceName,exa_field_name=service_name""",
    """exa_json_path=$..Success,exa_field_name=result""",
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..customerIDString,exa_field_name=cid""",
    """exa_json_path=$.event..user_agent,exa_field_name=user_agent""",
    """exa_json_path=$.event..request_path,exa_field_name=uri_path""",
    """exa_json_path=$.event..status_code,exa_regex=({http_response_code}\d+)""",
    """exa_json_path=$.event..request_query,exa_field_name=uri_query""",
    """exa_json_path=$.event..request_method,exa_field_name=method""",
    """exa_json_path=$.event..scopes,exa_field_name=assignble_scope""",
    """exa_json_path=$..OperationName,exa_field_name=operation""",
    """exa_json_path=$..eventType,exa_field_name=operation_details"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'request_path')].ValueString,exa_field_name=uri_path"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'trace_id')].ValueString,exa_field_name=tracking_id"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'cid')].ValueString,exa_field_name=cid"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'status_code')].ValueString,exa_field_name=http_response_code"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'user_agent')].ValueString,exa_field_name=user_agent"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'request_method')].ValueString,exa_field_name=method"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'APIClientID')].ValueString,exa_field_name=app_id"""
    """exa_json_path=$.AuditKeyValues[?(@.Key == 'produces')].ValueString,exa_field_name=mime"""
  ]
  ParserVersion = "v1.0.0"


}
```