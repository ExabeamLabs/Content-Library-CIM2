#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-login-authentication
  ParserVersion = "v1.0.0"
  Conditions = [ """"destinationServiceName":"CrowdStrike"""", """"ServiceName":"Crowdstrike Authentication"""" ]
  Fields = ${DLCrowdStrikeParserTemplates.json-crowdstrike-app-login.Fields}[
    """"destinationServiceName":"(|({app}.+?))"(\s+\w+=|\s*$)?"""
  ]

json-crowdstrike-app-login = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """\Wsuser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """"UserIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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