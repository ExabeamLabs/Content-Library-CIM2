#### Parser Content
```Java
{
Name = "microsoft-azuread-xml-user-password-reset-success-10015-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>10015</eventid>"
      "microsoft-azureadpasswordprotection-dcagent"
      " username:"
      "the reset password for the specified user was validated as compliant with the current azure password policy"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d\\-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'/>"
      "(?i)<Data Name ='Data1'>({user}[^<]+)</Data>"
      "(?i)<Data Name ='Data2'>({full_name}[^<]+)</Data>"
      "(?i)<EventID>({event_code}10015)</EventID>"
      "(?i)({event_name}The reset password for the specified user was validated as compliant with the current Azure password policy)"
      "(?i)<Keywords>({result}[^<]+)</Keywords>"
      "(?i)Security UserID='({user_sid}[^']+)'"
      "(?i)<Message>({additional_info}[^<]+?)\\s+</Message>"
    ]
  

}
```