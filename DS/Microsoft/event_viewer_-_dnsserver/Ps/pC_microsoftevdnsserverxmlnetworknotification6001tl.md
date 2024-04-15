#### Parser Content
```Java
{
Name = "microsoft-evdnsserver-xml-network-notification-6001-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - DNSServer"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      ">6001</eventid>"
      "dns_event_zonexfr_successful"
      "<provider>microsoft-windows-dns-server-service</provider>"
      "<channel>dns server</channel>"
    ]
    Fields = [
      "(?i)<Message>({additional_info}[^<>]+)</Message>"
      "(?i)>({event_code}[^<>]+)</EventID>"
      "(?i)EventData Name ='({event_name}[^>']+)"
      "(?i)<Computer>({host}[^<>]+)</Computer>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)<Security UserID='({user_sid}[^']+)"
      "(?i)Guid='\\{({process_guid}[^}']+?)\\}'"
      "(?i)ProcessID='({process_id}\\d+)"
    ]
  

}
```