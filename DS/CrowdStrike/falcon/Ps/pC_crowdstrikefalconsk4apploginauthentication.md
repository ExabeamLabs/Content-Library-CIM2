#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-login-authentication
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =CrowdStrike""", """"ServiceName":"CrowdStrike Authentication"""" ]
  Fields = ${DLCrowdStrikeParserTemplates.json-crowdstrike-app-login.Fields}[
    """\WdestinationServiceName =(|({app}.+?))(\s+\w+=|\s*$)""",
  ]

json-crowdstrike-app-login = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """\Wsuser=(|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """"UserIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"Success":({result}\w+)""",
    """"ServiceName":"({service_name}[^"]+)""",
    """"UserId":"({user_id}[^"]+)""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"FalconHostLink":"({additional_info}[^"]+)""",
    """"OperationName":"({operation}[^"]+)""",
    """"EventType":"({event_category}[^"]+)""",
# api_type is removed
  
}
```