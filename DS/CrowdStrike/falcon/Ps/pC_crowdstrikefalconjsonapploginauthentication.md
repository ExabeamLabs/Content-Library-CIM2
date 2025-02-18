#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-login-authentication
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """AuthActivityAuditEvent""", """"ServiceName":"Crowdstrike Authentication"""" ]
  Fields = ${DLCrowdStrikeParserTemplates.json-crowdstrike-app-login.Fields}[
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_regex="eventCreationTime":({time}\d{13})"""
    """exa_json_path=$.destinationServiceName,exa_field_name=app"""
  ]

json-crowdstrike-app-login = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","epoch"]
  Fields = [
    """\Wsuser=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """"UserIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"Success":({result}\w+)""",
    """"ServiceName":"({service_name}[^"]+)""",
    """"UserId":"({user_id}[^"]+)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"FalconHostLink":"({additional_info}[^"]+)""",
    """"OperationName":"({operation}[^"]+)""",
    """"EventType":"({event_category}[^"]+)""",
    """"cid":"({cid}[^"]+)""""
    """"customerIDString":"({cid}[^"]+)""""
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..customerIDString,exa_field_name=cid""",
    """exa_json_path=$.event.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	  """exa_json_path=$.event.Success,exa_field_name=result""",
    """exa_json_path=$.event.ServiceName,exa_field_name=service_name""",
    """exa_json_path=$.event.UserId,exa_field_name=user_id""",
    """exa_json_path=$.event.OperationName,exa_field_name=operation""",
    """exa_json_path=$.metadata.eventType,exa_field_name=event_category"""
# api_type is removed
  
}
```