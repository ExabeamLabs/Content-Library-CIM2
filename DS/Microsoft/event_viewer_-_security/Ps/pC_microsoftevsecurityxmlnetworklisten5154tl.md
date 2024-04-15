#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-listen-5154-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>5154<"
      "the windows filtering platform has permitted an application or service to listen on a port for incoming connections"
    ]
    Fields = [
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)({event_name}The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections.)"
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)"
      "(?i)<Data Name ='Protocol'>({protocol}[^<>]+?)<\\/Data>"
      "(?i)<Data Name ='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Data Name ='SourcePort'>(0|({src_port}\\d+))"
      "(?i)<Data Name ='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?"
      "(?i)<Data Name ='DestPort'>(0|({dest_port}\\d+))"
      "(?i)\\sProcess ID:\\s*(|-|({process_id}.+?))\\s*Application Name:\\s*(|-|({app}.+?))\\s*Network Information"
    ]
  

}
```