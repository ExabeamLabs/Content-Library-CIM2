#### Parser Content
```Java
{
Name = microsoft-azure-sk4-app-activity-adduser
  Conditions = [ """"ActivityDisplayName":"Add user"""", """"OperationName":"Add user"""", """"ActivityDateTime":"""", """"ResourceId":"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${MSParsersTemplates.azure-app-activity-2.Fields}[
    """({operation}Add user)"""
  ]

azure-app-activity-2 {
    Vendor = Microsoft
    Product = Azure Monitor
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    Fields = [
      """"ActivityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?(Z|[+-]\d\d:\d\d))"""",
      """"Result":"({result}[^"]+)"""",
      """"resultReason":"({failure_reason}[^"]+)"""",
      """"ActivityDisplayName":"({event_name}[^"]+)"""",
      """"ResourceId":"({object}[^"]+)"""",
      """"resourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)"""
      """"value\\":\\"({user_agent}[^"]+?)\\?",\\"key\\":\\"User-Agent\\"""",
      """"key\\":\\"User-Agent\\",\\"value\\":\\"({user_agent}[^"]+?)\\?"""",
      """"InitiatedBy":"\{\\"user\\":\{[^\}]+"userPrincipalName\\":\\"({email_address}[^@"]+@[^\."]+\.[^"]+?)\\?"""",
      """CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"InitiatedBy":"\{\\"user\\":\{[^\}]+"ipAddress\\":\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?"""",
      """"LoggedByService":"(Core Directory|({app}[^"]+))"""",
      """TargetResources":"\[[^|]+userPrincipalName\\":\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"""",
      """destinationServiceName =({app}Azure)""",
      """"app":\{[^,]+,"displayName":"({app}[^"]+)""""
      """Category":"({category}[^"]+)""",
      """"Type":"({event_category}[^"]+)""",
      """"type":"({additional_info}[^"]+)""",
      """"Resource":"({resource}[^"]+)""",
    ]
   DupFields = [ "event_name->operation" 
}
```