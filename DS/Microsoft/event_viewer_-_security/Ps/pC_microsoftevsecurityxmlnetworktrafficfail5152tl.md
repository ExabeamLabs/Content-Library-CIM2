#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-traffic-fail-5152-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5152<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID(\\\\)?='({process_id}\\d+)"
      "(?i)<Task>({task_name}[^<]+)"
      "(?i)<Keywords>({result}[^<]+)"
      "(?i)<Data Name(\\\\)?='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name(\\\\)?='SourcePort'>({src_port}\\d+)"
      "(?i)<Data Name(\\\\)?='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<Data Name(\\\\)?='DestPort'>({dest_port}\\d+)"
      "(?i)<Data Name(\\\\)?='Protocol'>({protocol}[^<]+)"
      "(?i)({event_name}the windows filtering platform has blocked a packet)"
    ]
  

}
```