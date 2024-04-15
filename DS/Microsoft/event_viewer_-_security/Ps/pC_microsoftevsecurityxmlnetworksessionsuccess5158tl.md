#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-success-5158-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5158</eventid>"
      "<event xmlns"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime\\\\*='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d+Z'/>"
      "(?i)({event_code}5158)"
      "(?i)<Computer>({host}[^<>]+?)</Computer>"
      "(?i)<Data Name\\\\*='ProcessId'>({process_id}[^<>]+)</Data>"
      "(?i)<Data Name\\\\*='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/]+?))</Data>"
      "(?i)<Data Name\\\\*='SourceAddress'>(::|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)</Data>"
      "(?i)<Data Name\\\\*='SourcePort'>({src_port}\\d+)</Data>"
      "(?i)<Data Name\\\\*='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?</Data>"
      "(?i)<Data Name\\\\*='DestPort'>({dest_port}\\d+)</Data>"
      "(?i)<Data Name\\\\*='Protocol'>({ms_protocol_num}\\d+)</Data>"
      "(?i)<Data Name\\\\*='LayerName'>\\s*({layer_name}[^<]+?)\\s*</Data>"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```