#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-dns-request-success-query-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Sysmon"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<provider name='microsoft-windows-sysmon'"
      "<eventid>22</eventid>"
      "<channel>microsoft-windows-sysmon/operational</channel>"
      "<data name="
    ]
    Fields = [
      "(?i)<Data Name ='UtcTime'>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)</Data>"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Computer>({host}.+?)</Computer>"
      "(?i)<Security UserID='({user_sid}.+?)'/>"
      "(?i)(?i)<Data Name ='ProcessGuid'>\\{({process_guid}[A-F0-9a-f-]+)\\}</Data>"
      "(?i)<Data Name ='ProcessId'>({process_id}\\d+)</Data>"
      "(?i)<Data Name ='QueryName'>({dns_query}.+?)\\s*</Data>"
      "(?i)<Data Name ='QueryResults'>({dns_response}.+?)\\s*</Data>"
      "(?i)<Data Name ='Image'>({path}(({process_dir}[^<]*)\\+)?({process_name}.+?))</Data>"
    ]
  

}
```