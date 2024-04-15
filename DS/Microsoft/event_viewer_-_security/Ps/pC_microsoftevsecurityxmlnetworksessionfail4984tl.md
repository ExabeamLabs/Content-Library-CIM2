#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-fail-4984-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4984<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)<Task>({task_name}[^<]+)"
      "(?i)<Data Name ='LocalAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name ='LocalKeyModPort'>({src_port}\\d+)"
      "(?i)<Data Name ='RemoteAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<Data Name ='RemoteKeyModPort'>({dest_port}\\d+)"
      "(?i)<Data Name ='FailureReason'>({failure_reason}[^<]+)"
      "(?i)<Data Name ='State'>({state}[^<]+)"
      "(?i)<Data Name ='Role'>({role}[^<]+)"
      "(?i)<Keywords>({action}[^<]+)"
    ]
  

}
```