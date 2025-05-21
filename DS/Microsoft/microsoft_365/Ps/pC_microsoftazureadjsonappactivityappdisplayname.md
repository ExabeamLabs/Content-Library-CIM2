#### Parser Content
```Java
{
Name = microsoft-azuread-json-app-activity-appdisplayname
  Vendor = "Microsoft"
  Product = "Microsoft 365"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """"resourceDisplayName""", """"appDisplayName"""", """riskLevelDuringSignIn""", """userPrincipalName"""  ]
  Fields = [
    """"createdDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """({event_name}Sign-In)""",
    """"userId":"({user_id}[^"]+)"""
    """"appDisplayName":"({app}[^"]+)"""
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d{1,20}))?"""
    """"clientAppUsed":"({object}[^"]+)"""
    """"resourceDisplayName":"({resource}[^",]+)"""
    """"additionalDetails":"({additional_info}[^"]+)"""
    """"deviceDetail".+?operatingSystem":"({os}[^"]+)"""
    """"location".+?city":"({location_city}[^",]+)"""
    """"location".+?state":"({location_state}[^",]+)"""
    """"location".+?countryOrRegion":"({location_country}[^",]+)"""
    """"failureReason":"(Other|({failure_reason}[^"]+))"""
    """"errorCode":({error_code}\d+)"""
    """"userDisplayName":"(({full_name}[^\s"]+\s+[^"]+)|({user_id}[^"]+))"""
    """"+userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))""""
  ]


}
```