#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-login-apiactivityauditevent
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = ["epoch_sec", "epoch"]
  Conditions = [ """"eventType":""", """"OperationName":""", """APIActivityAuditEvent""" ]
  Fields = [
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_json_path=$.event.UTCTimestamp,exa_field_name=time""",
    """exa_json_path=$.event.SessionId,exa_field_name=session_id""",
    """exa_json_path=$.event.UserId,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.event.UserName,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.event.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.event.ServiceName,exa_field_name=service_name""",
    """exa_json_path=$.event.Success,exa_field_name=result""",
    """exa_json_path=$.event..cid,exa_field_name=cid""",
    """exa_json_path=$.metadata.customerIDString,exa_field_name=cid""",
    """exa_json_path=$.event..user_agent,exa_field_name=user_agent""",
    """exa_json_path=$.event..request_path,exa_field_name=uri_path""",
    """exa_json_path=$.event..status_code,exa_field_name=http_response_code""",
    """exa_json_path=$.event..request_query,exa_field_name=uri_query""",
    """exa_json_path=$.event..request_method,exa_field_name=method""",
    """exa_json_path=$.event..scopes,exa_field_name=assignble_scope""",
    """exa_json_path=$.event.OperationName,exa_field_name=operation""",
    """exa_json_path=$.metadata.eventType,exa_field_name=operation_details"""
  ]
  ParserVersion = "v1.0.0"


}
```