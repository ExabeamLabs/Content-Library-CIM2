#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-app-login-success-startevent"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
  """"eventType":"""
  """"RemoteResponseSessionStartEvent""""
  """UserName"""
]
Fields = [
  """"eventCreationTime":\s*({time}\d{10})"""
  """"timestamp":"({time}\d{10})""""
  """"UTCTimestamp":({time}\d{10})"""
  """"UserId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"ServiceName":\s*"({app}[^"]+)"""
  """"Success":\s*({result}[^",}]+)"""
  """"UserName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"UserName":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"HostnameField":\s*"({host}[^"@]+)""""
  """destinationServiceName =({app}[^=]+)\s\w+="""
  """"destinationServiceName":"({app}[^=]+?)"(\s\w+=)?"""
  """({event_name}RemoteResponseSessionStartEvent)"""
  """"SessionId":"({session_id}[^",]+)""""
  """"(?i)EventType":\s*"({operation_details}[^",]+)""""
]
DupFields = [
  "event_name->operation"
  "host->src_host"
]
ParserVersion = "v1.0.0"


}
```