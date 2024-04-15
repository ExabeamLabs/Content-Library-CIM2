#### Parser Content
```Java
{
Name = "microsoft-evadfs-xml-rdp-traffic-success-1149-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - ADFS"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>1149<"
      "<security userid="
      "<param1>"
      "<computer>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)'"
      "(?i)<Computer>({host}[\\w\\-.]+)<"
      "(?i)({event_code}1149)"
      "(?i)<Param1>({user}[^<@]+)(@({domain}[^<]+))?<"
      "(?i)<Param2>({domain}[^<]+)<"
      "(?i)<Param3>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<"
      "(?i)<Security UserID='({user_sid}[^']+)'"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```