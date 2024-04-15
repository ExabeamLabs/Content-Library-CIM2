#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-activity-5451-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5451<"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Execution ProcessID='({process_id}\\d+)"
      "(?i)<Task>({task_name}[^<]+)"
      "(?i)<Keywords>({result}[^<]+)"
      "(?i)<Data Name ='LocalAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name ='RemoteAddress'>(-|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?)"
      "(?i)<Data Name ='LocalPort'>({src_port}\\d+)"
      "(?i)<Data Name ='LocalTunnelEndpoint'>({src_translated_ip}[^<]+)"
      "(?i)<Data Name ='RemotePort'>({dest_port}\\d+)"
      "(?i)<Data Name ='RemoteTunnelEndpoint'>({dest_translated_ip}[^<]+)"
      "(?i)<Data Name ='LifetimeSeconds'>({duration}[^<]+)"
      "(?i)<Data Name ='Role'>({role}[^<]+)"
    ]
  

}
```