#### Parser Content
```Java
{
Name = "microsoft-evazureadppdca-xml-app-notification-30006-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "the service is now enforcing the following azure password policy"
      "<eventid>30006</eventid>"
      "microsoft-azureadpasswordprotection-dcagent"
    ]
    Fields = [
      "(?i)<TimeCreated\\sSystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d+Z)"
      "(?i)<Computer>({host}[^<]+)<\\/Computer>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)({event_name}The service is now enforcing the following Azure password policy)"
      "(?i)<Security\\sUserID='({user_sid}[^']+)'"
      "(?i)<Keywords>({result}[^<]+)<\\/Keywords>"
      "(?i)<Execution\\sProcessID='({process_id}[^']+)'"
      "(?i)ThreadID='({thread_id}[^']+)'"
      "(?i)<Message>({additional_info}[^\\n]+?)\\s*<\\/Message>"
    ]
    DupFields = [
      "event_name->operation"
    ]
  

}
```