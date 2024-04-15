#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-fail-5157-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<eventid>5157</eventid>"
      "<event xmlns"
    ]
    Fields = [
      "(?i)({event_name}The Windows Filtering Platform has blocked a connection)"
      "(?i)<TimeCreated SystemTime(\\\\)?='({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)\\d{1,100}Z'/>"
      "(?i)<EventID>({event_code}5157)<"
      "(?i)<Computer>({host}[^<>]{1,2000})</Computer>"
      "(?i)<Data Name(\\\\)?='ProcessID'>({process_id}[^<>]{1,2000})<\\/Data>"
      "(?i)<Data Name(\\\\)?='Application'>({process_path}({process_dir}(?:[^<]{1,2000})?[\\\\\\/])?({process_name}[^\\\\\\/]{1,2000}?))<\\/Data>"
      "(?i)<Data Name(\\\\)?='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name(\\\\)?='SourcePort'>({src_port}\\d{1,100})</Data>"
      "(?i)<Data Name(\\\\)?='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?</Data>"
      "(?i)<Data Name(\\\\)?='DestPort'>({dest_port}\\d{1,100})</Data>"
      "(?i)<Data Name(\\\\)?='Protocol'>({protocol}[^<>]{1,2000})</Data>"
      "(?i)<RenderingInfo.+?<Task>({operation_type}[^<>]{1,2000})</Task>.*?</RenderingInfo>"
      "(?i)<Computer>({src_host}[^<>]{1,2000})</Computer>.+?Direction:\\s{0,100}({direction}Outbound)"
      "(?i)<Computer>({dest_host}[^<>]{1,2000})</Computer>.+?Direction:\\s{0,100}({direction}Inbound)"
      "(?i)<Data Name(\\\\)?='LayerName'>({layer_name}[^<]{1,2000})"
    ]
    DupFields = [
      "host->local_asset"
    ]
  

}
```