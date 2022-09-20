#### Parser Content
```Java
{
Name = microsoft-azure-sk4-app-activity-addownertogroup
  Conditions = [ """"ActivityDisplayName":"Add owner to group"""", """"OperationName":"Add owner to group"""", """"ActivityDateTime":"""", """"ResourceId":"""" ]
  Fields = ${MSParsersTemplates.azure-app-activity-2.Fields}[
  """Group\.ObjectID\\"[^\}]+?"newValue\\":\\"\\+"({object}[^"\\]+)"""
  ]
  ParserVersion = "v1.0.0"

azure-app-activity-2 {
    Vendor = Microsoft
    Product = Azure
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"ActivityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"""",
      """"Result":"({result}[^"]+)"""",
      """"ActivityDisplayName":"({event_name}[^"]+)"""",
      """"ResourceId":"({object}[^"]+)"""",
      """"value\\":\\"({user_agent}[^"]+?)\\?",\\"key\\":\\"User-Agent\\"""",
      """"key\\":\\"User-Agent\\",\\"value\\":\\"({user_agent}[^"]+?)\\?"""",
      """"InitiatedBy":"\{\\"user\\":\{[^\}]+"userPrincipalName\\":\\"({email_address}[^@"]+@[^\."]+\.[^"]+?)\\?"""",
      """"InitiatedBy":"\{\\"user\\":\{[^\}]+"ipAddress\\":\\"({src_ip}[A-Fa-f:\d.]+?)\\?"""",
      """"LoggedByService":"(Core Directory|({app}[^"]+))"""",
      """TargetResources":"\[[^|]+userPrincipalName\\":\\"({dest_user}[^"]+?)\\?"""",
      """"app":\{[^,]+,"displayName":"({app}[^"]+)""""
    ]
   DupFields = [ "event_name->operation" 
}
```