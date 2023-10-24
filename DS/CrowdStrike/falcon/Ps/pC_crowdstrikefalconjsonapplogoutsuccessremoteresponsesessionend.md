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
  ]
  DupFields = [ "operation_details->operation" ]

json-crowdstrike-app-logout = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"HostnameField":\s*"({host}[^"@]+)"""",
    """"eventCreationTime":\s*({time}\d{10})""",
    """"timestamp":"({time}[^",]\d{10})"""",
    """"SessionId":"({session_id}[^",]+)"""",
    """"UserName":\s*"({email_address}[^"@]+@[^"@]+)"""",
    """"UserName":\s*"({user}[\w\.\-]{1,40}\$?)""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ServiceName":\s*"({app}[^"]+)""",
    """"Success":\s*({result}[^",}]+)""",
    """"OperationName":"({event_name}[^"]+)""",
    """"Commands":\s*({additional_info}\[[^\]\{]+\])""",
    """"AgentIdString":"({aid}[^",]+)"""",
    """"(?i)EventType":\s*"({operation_details}[^",]+)"""",
	  """"ExternalApiType":\s*"({operation}[^"]+)""""
  
}
```