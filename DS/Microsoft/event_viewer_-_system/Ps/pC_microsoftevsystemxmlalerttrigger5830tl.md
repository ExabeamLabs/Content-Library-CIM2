#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-alert-trigger-5830-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      ">5829</eventid>"
      "netlogon"
      "<eventdata><data>"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<\\.]+)\\.({domain}[^<]+)<"
      "(?i)SystemTime=(?:[\"']+)?({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventID[^>]+>({event_code}\\d+)<"
      "(?i)<Provider Name =(?:[\"']+)?({provider_name}[\\w-]+)"
      "(?i)<Level>({alert_severity}\\d+)"
      "(?i)<Keywords>({result}[^<]+)<"
      "(?i)<EventRecordID>({event_id}\\d+)"
      "(?i)<EventData><Data>([^<]+)<\\/Data><Data>({domain}[^<]+?)\\.*<\\/Data><Data>({user_type}[^<]+)<\\/Data><Data>({os}[^<]+)<\\/Data><Data>([^<]+)<\\/Data><Data>(?:(?i)N\\/A|([^<]+))<"
    ]
  

}
```