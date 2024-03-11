#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-login-success-snowflake
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """destinationServiceName =Snowflake""", """"appDisplayName":"""", """"result":"""", """"enforcedGrantControls":"""", """"resourceDisplayName":"""" ]
  Fields =[
    """"createdDateTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d{1,3})"""",
    """"additionalDetails":"({event_name}[^"]+)"""",
    """"appDisplayName":"({app}[^"]+)"""",
    """"conditionalAccessStatus":"({result}[^"]+)"""",
    """"userDisplayName":"({full_name}[^"]+)"""",    
    """"userPrincipalName":"({email_address}[^@"]+@[^"]+)"""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"countryOrRegion":"({location_country}[^"]+)"""",
    """"city":"({location_city}[^"]+)"""",
    """"state":"({location_state}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```