#### Parser Content
```Java
{
Name = "microsoft-azuread-xml-user-password-modify-success-10024-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>10024</eventid>"
      "<provider name='microsoft-azureadpasswordprotection-dcagent'"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{1,10}Z)'/>"
      "(?i)<Data Name ='Data1'>({user}[^<]+)</Data>"
      "(?i)<Data Name ='Data2'>({full_name}[^<]+)</Data>"
      "(?i)<EventID>({event_code}10024)</EventID>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)Security UserID='({user_sid}[^']+)'"
      "(?i)<Message>({additional_info}({event_name}[^<\\.]+?)\\.[^<]+?)\\s+</Message>"
    ]
    DupFields = [
      "user->dest_user"
    ]
  

}
```