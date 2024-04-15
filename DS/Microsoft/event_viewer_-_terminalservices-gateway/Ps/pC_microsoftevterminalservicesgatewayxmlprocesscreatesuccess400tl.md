#### Parser Content
```Java
{
Name = "microsoft-evterminalservicesgateway-xml-process-create-success-400-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - TerminalServices-Gateway"
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [
      ">windows powershell<"
      "<message>engine state is changed from none to available"
      "engine lifecycle"
      ">400</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)\\.\\d+Z'\\/>"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)\\sHostApplication=({process_path}({process_name}[^\\s\\\\\\/]+)[^=]*?)\\s+EngineVersion="
      "(?i)({event_name}Engine state is changed from None to Available)"
      "(?i)({event_code}\\d+)<\\/EventID>"
      "(?i)<Keywords>({result}[^<]+)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
    ]
    DupFields = [
      "host->src_host"
      "process_path->process_command_line"
    ]
    ParserVersion = "v1.0.0"
  

}
```