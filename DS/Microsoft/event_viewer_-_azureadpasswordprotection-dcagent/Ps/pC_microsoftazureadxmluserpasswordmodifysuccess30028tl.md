#### Parser Content
```Java
{
Name = "microsoft-azuread-xml-user-password-modify-success-30028-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>30028</eventid>"
      "'microsoft-azureadpasswordprotection-dcagent'"
      " username:"
    ]
    Fields = [
      "(?i)<EventID>({event_code}30028)</EventID>"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'/>"
      "(?i)<Message>({event_name}[^.<]+)"
      "(?i)UserName:\\s*({user}[^\\s]+)"
      "(?i)FullName:\\s+({full_name}[^<]+?)\\s+</Message>"
      "(?i)Security UserID='({user_sid}[^']+)'"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
    ]
  

}
```