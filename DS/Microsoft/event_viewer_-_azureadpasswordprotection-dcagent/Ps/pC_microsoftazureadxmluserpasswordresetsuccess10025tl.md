#### Parser Content
```Java
{
Name = "microsoft-azuread-xml-user-password-reset-success-10025-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>10025</eventid>"
      "<provider name='microsoft-azureadpasswordprotection-dcagent'"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'/>"
      "(?i)<Data Name ='Data1'>({user}[^<]+)</Data>"
      "(?i)<Data Name ='Data2'>({full_name}[^<]+)</Data>"
      "(?i)<EventID>({event_code}10025)</EventID>"
      "(?i)<Keywords>({action}[^<]+)</Keywords>"
      "(?i)Security UserID='({user_sid}[^']+)'"
      "(?i)<Message>({additional_info}({event_name}[^<\\.]+?)\\.[^<]+?)\\s+</Message>"
    ]
    DupFields = [
      "user->dest_user"
    ]
  

}
```