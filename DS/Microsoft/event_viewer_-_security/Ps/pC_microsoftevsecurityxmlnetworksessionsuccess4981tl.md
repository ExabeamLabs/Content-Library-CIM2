#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-success-4981-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4981<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)<Task>({task_name}[^<]+)"
      "(?i)<Data Name ='LocalMMPrincipalName'>({src_host}[^<]+)"
      "(?i)<Data Name ='RemoteMMPrincipalName'>({dest_host}[^<]+)"
      "(?i)<Data Name ='LocalAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name ='LocalKeyModPort'>({src_port}\\d+)"
      "(?i)<Data Name ='RemoteAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<Data Name ='RemoteKeyModPort'>({dest_port}\\d+)"
      "(?i)<Data Name ='MMLifetime'>({duration}[^<]+)"
      "(?i)<Keywords>({action}[^<]+)"
    ]
  

}
```