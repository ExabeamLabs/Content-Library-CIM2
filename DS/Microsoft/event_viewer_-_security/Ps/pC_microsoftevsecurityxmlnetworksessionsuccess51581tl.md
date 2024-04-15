#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-success-5158-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "5158"
      "<data name='"
      "the windows filtering platform has permitted a bind to a local port"
    ]
    Fields = [
      "(?i)\"TimeGenerated\":\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_code}5158)"
      "(?i)\"Activity\":\"({event_name}[^\"]+)"
      "(?i)\"Computer\":\"({host}[^\"]+)"
      "(?i)<Data Name ='ProcessId'>({process_id}.+?)</Data>"
      "(?i)<Data Name ='Application'>({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^\"\\\\\\/]+))</Data>"
      "(?i)<Data Name ='SourceAddress'>(0\\.0\\.0\\.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?)</Data>"
      "(?i)<Data Name ='SourcePort'>({dest_port}\\d+)"
      "(?i)<Data Name ='Protocol'>({ms_protocol_num}.+?)</Data>"
      "(?i)<Data Name ='LayerName'>({layer_name}.+?)</Data>"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```