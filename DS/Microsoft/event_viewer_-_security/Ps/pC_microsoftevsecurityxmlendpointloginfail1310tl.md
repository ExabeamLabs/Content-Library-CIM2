#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-fail-1310-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid qualifiers='16640'>1310<"
      "failed ntlm authentication"
    ]
    Fields = [
      "(?i)<Provider Name ='({provider_name}[^']+)"
      "(?i)<EventID Qualifiers='16640'>({event_code}[^<]+)"
      "(?i)<Keywords>({result}[^<]+)"
      "(?i)<TimeCreated SystemTime='({time}.+?)'"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)status=([^:]+:)({result_code}[^:]+):"
      "(?i)Failed NTLM Authentication for user:\\s+'({domain}[^\\\\]+)\\\\({user}[^']+)"
      "(?i)<Message>({event_name}.+?)\\s{0,100}<"
      "(?i)status=([^:]+:){2}({failure_reason}.+?)\\s<"
    ]
    DupFields = [
      "host->dest_host"
      "result_code->failure_code"
    ]
  

}
```