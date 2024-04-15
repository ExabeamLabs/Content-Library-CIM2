#### Parser Content
```Java
{
Name = "microsoft-evapplocker-xml-alert-trigger-success-policyname-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Applocker"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<channel>microsoft-windows-applocker"
      "<policyname>"
      "<message>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)<Data Name ='User'>(({domain}[^\\\\<]+?)\\\\)?({user}.+?)</Data>"
      "(?i)<Security UserID='({user_sid}.+?)'/>"
      "(?i)<Level>({alert_severity}[^\"<]+)"
      "(?i)<FilePath>({malware_url}[^\"<]+)"
      "(?i)<PolicyName>({alert_type}[^\"<]+)"
      "(?i)<PolicyName>({alert_name}[^\"<]+)"
      "(?i)<Message>({additional_info}[^\"<]+)"
      "(?i)<FileHash>({hash_md5}[^\"<]+)"
    ]
    DupFields = [
      "malware_url->process_name"
    ]
    ParserVersion = "v1.0.0"
  

}
```