#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-login-fail-snowflake
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """destinationServiceName =Snowflake""", """"appDisplayName":"""", """"result":"failure"""", """"enforcedGrantControls":"""", """"resourceDisplayName":"""" ]
  Fields =[
    """"createdDateTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d{1,3})"""",
    """"additionalDetails":"({event_name}[^"]+)"""",
    """"appDisplayName":"({app}[^"]+)"""",
    """"conditionalAccessStatus":"({result}[^"]{,2000})"""",
    """"userDisplayName":"({full_name}[^"]+)"""",
    """"userPrincipalName":"({email_address}[^@"]+@[^"]+)"""",
    """"ipAddress":"({src_ip}[a-fA-F\d:.]+)"""",
    """"countryOrRegion":"({location_country}[^"]+)"""",
    """"city":"({location_city}[^"]+)"""",
    """"state":"({location_state}[^"]+)"""",
    """"displayName":"({failure_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```