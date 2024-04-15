#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-fail-5157-1-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "\"eventid\":\"5157\""
      "<data name='"
    ]
    Fields = [
      "(?i)({event_name}The Windows Filtering Platform has blocked a connection)"
      "(?i)\"TimeGenerated\":\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_code}5157)"
      "(?i)\"Computer\":\"({host}[^\"]+)"
      "(?i)<Data Name ='ProcessID'>({process_id}[^<>]+)<\\/Data>"
      "(?i)<Data Name ='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\\\\/])?({process_name}[^\\\\\\/]+?))<\\/Data>"
      "(?i)<Data Name ='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</Data>"
      "(?i)<Data Name ='SourcePort'>(0|({src_port}\\d+))</Data>"
      "(?i)<Data Name ='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?</Data>"
      "(?i)<Data Name ='DestPort'>(0|({dest_port}\\d+))</Data>"
      "(?i)<Data Name ='Protocol'>({protocol}[^<>]+)</Data>"
      "(?i)<RenderingInfo.+?<Task>({operation_type}[^<>]+)</Task>.*?</RenderingInfo>"
      "(?i)<Data Name ='Direction'>({direction}[^<>]+)</Data>"
      "(?i)<Data Name ='LayerName'>({layer_name}[^<>]+)</Data>"
    ]
    DupFields = [
      "host->local_asset"
    ]
    ParserVersion = "v1.0.0"
  

}
```