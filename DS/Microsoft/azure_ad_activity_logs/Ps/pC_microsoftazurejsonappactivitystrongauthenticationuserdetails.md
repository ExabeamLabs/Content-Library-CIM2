#### Parser Content
```Java
{
Name = "microsoft-azure-json-app-activity-strongauthenticationuserdetails"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [ """"activityDisplayName":"Update user"""", """"operationType":"Update"""", """"activityDateTime":"""", """StrongAuthenticationUserDetails""", """VoiceOnlyPhoneNumber""" ]
Fields = [
  """\"activityDateTime\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[+-]\d\d:\d\d)\""""
  """\"result\":\"({result}[^\"]+)\""""
  """\"activityDisplayName\":\"({event_name}[^\"]+)\""""
  """\"operationType\":\"({operation}[^\"]+)\""""
  """\"user\":\{\"id\":\"({user_id}[^\"]+)\""""
  """\"initiatedBy\"[^]]+\"userPrincipalName\":\"({email_address}({user}[^@\"]+)@[^\.\"]+\.[^\"]+)\""""
  """targetResources[^}]+\"userPrincipalName\":\"({dest_user}[^@\"]+)"""
  """\"resourceId\":\"({object}[^\"]+)\""""
  """\"newValue\":\"\[({additional_info}\{[\\]?\"PhoneNumber[^]]+)"""
]
ParserVersion = "v1.0.0"


}
```