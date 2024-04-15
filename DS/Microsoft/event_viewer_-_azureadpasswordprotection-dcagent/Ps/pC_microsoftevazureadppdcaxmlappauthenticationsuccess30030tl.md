#### Parser Content
```Java
{
Name = "microsoft-evazureadppdca-xml-app-authentication-success-30030-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>30030</eventid>"
      "microsoft-azureadpasswordprotection-dcagent"
      "<computer>"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'/>"
      "(?i)<EventID>({event_code}30030)</EventID>"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)Security UserID='({user_sid}[^']+)'"
      "(?i)<Message>({event_name}[^<\\.:]+?)(<|\\.|:)"
    ]
  

}
```