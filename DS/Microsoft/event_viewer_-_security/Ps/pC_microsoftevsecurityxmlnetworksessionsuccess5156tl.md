#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-success-5156-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5156</eventid>"
      "<event xmlns"
    ]
    Fields = [
      "(?i)({event_name}The Windows Filtering Platform has permitted a connection)"
      "(?i)<TimeCreated SystemTime\\\\*='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)({event_code}5156)"
      "(?i)<Computer>({host}[^<>]+)</Computer>"
      "(?i)<Data Name\\\\*='ProcessID'>({process_id}[^<>]+)<\\/Data>"
      "(?i)<Data Name\\\\*='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/]+?))<\\/Data>"
      "(?i)<Data Name\\\\*='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name\\\\*='SourcePort'>({src_port}\\d+)</Data>"
      "(?i)<Data Name\\\\*='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?<\\/Data>"
      "(?i)<Data Name\\\\*='DestPort'>({dest_port}\\d+)<\\/Data>"
      "(?i)<Data Name\\\\*='Protocol'>({protocol}[^<>]+)<\\/Data>"
      "(?i)<RenderingInfo[^$]+?<Task>({operation_type}}[^<>]+)</Task>[^$]*?</RenderingInfo>"
      "(?i)<Computer>({src_host}[^<>]+)</Computer>[^$]+?Direction:\\s*({direction}Outbound)"
      "(?i)<Computer>({dest_host}[^<>]+)</Computer>[^$]+?Direction:\\s*({direction}Inbound)"
      "(?i)Layer Name:\\s*({layer_name}[^:]+?)(\\\\[rn]|\\s)"
    ]
    DupFields = [
      "host->local_asset"
    ]
  

}
```