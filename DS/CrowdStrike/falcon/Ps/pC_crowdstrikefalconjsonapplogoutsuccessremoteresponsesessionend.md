#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-logout-success-remoteresponsesessionend
  TimeFormat = "epoch"
  ParserVersion = v1.0.0
  Conditions = [ """"aid":""", """"aip":""", """"eventType":"RemoteResponseSessionEndEvent"""", """"UserName":"""]
  Fields = ${DLCrowdStrikeParserTemplates.json-crowdstrike-app-logout.Fields}[
    """"eventCreationTime":\s*({time}\d{13})""",    
    """"destinationServiceName":"({app}CrowdStrike)""""
    """"(?i)EventType":\s*"({operation}[^",]+)"""",
    """exa_json_path=$.metadata.eventType,exa_field_name=operation"""
  ]

json-crowdstrike-app-logout = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"HostnameField":\s*"({host}[^"@]+)"""",
    """Timestamp":\s*({time}\d{10})"""
    """"eventCreationTime":\s*({time}\d{10})""",
    """"timestamp":"({time}[^",]\d{10})"""",
    """"SessionId":"({session_id}[^",]+)"""",
    """"UserName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"UserName":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)""",
    """"OperationName":"({event_name}[^"]+)""",
    """"Commands":\s*({additional_info}\[[^\]\{]+\])""",
    """"AgentIdString":"({aid}[^",]+)"""",
    """"(?i)EventType":\s*"({operation_details}[^",]+)"""",
	  """"ExternalApiType":\s*"({operation}[^"]+)"""",
    """"cid":"({cid}[^"]+)""""
    """"customerIDString":"({cid}[^"]+)""""
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..customerIDString,exa_field_name=cid""",
    """exa_json_path=$.event.HostnameField,exa_field_name=host"""
    """exa_regex=Timestamp":\s*({time}\d{10})""",
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_regex="timestamp":"({time}[^",]\d{10})"""",
    """exa_json_path=$.event.SessionId,exa_field_name=session_id""",
    """exa_json_path=$.event.UserName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.event.UserName,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.event.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.event.ServiceName,exa_field_name=app""",
    """exa_json_path=$.event.Success,exa_field_name=result""",
    """exa_json_path=$.event.OperationName,exa_field_name=operation""",
    """exa_json_path=$.event.Commands[:0],exa_field_name=additional_info""",
    """exa_json_path=$.metadata.eventType,exa_field_name=operation_details"""
  
}
```