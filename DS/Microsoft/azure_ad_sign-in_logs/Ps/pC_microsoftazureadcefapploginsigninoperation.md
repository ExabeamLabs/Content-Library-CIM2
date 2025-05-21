#### Parser Content
```Java
{
Name = "microsoft-azuread-cef-app-login-signinoperation"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
ParserVersion = "v1.0.0"
Conditions = [ """Microsoft.aadiam""", """Sign-in activity""", """tenantId":""""]
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Fields = [
  """time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
  """initiatedBy":.+?userPrincipalName\":\"({email_address}[^@,:"]+@[^\.^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """initiatedBy":.+?id\":\"({user_uid}[^",]+)"""
  """callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """operationName":"({operation}[^\",]+)"""
  """result":"(notEnabled|notApplied|({result}[^",]+))"""
  """category":"({category}[^\",]+)\"*,correlationId""""
  """"app":"*?displayName\":\"({app}[^",]+)""""
  """loggedByService":"({app}[^\",]+)"""
  """({event_name}Sign-in operation)"""
  """userPrincipalName":"({email_address}[^@,:"]+@[^\.^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """userId":"({user_uid}[^\",]+)"""
  """errorCode":({error_code}\d+)"""
  """Level":({alert_severity}\d+)"""
  """appDisplayName\":\"\s*({app}[^\",]+)"""
  """deviceDetail.+?displayName\":\"({object}[^",]+)"""
  """userAgent":"({user_agent}.+?)\"?,\w+":"""
  """"failureReason":"({failure_reason}[^"]+)"""
]


}
```