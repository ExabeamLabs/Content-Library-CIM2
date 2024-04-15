#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-process-create-success-600-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [
      ">windows powershell<"
      "is started"
      "<task>provider lifecycle</task>"
      ">600</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)\\sHostApplication=({process_path}(|({process_dir}[^\\s]+?))({process_name}[^\\s\\\\\\/]+)[^=]*?)\\s+EngineVersion="
      "(?i)<Message>({event_name}[^:=<.]+)\\."
      "(?i)({event_code}\\d+)<"
      "(?i)<Keywords>({result}[^<]+)"
      "(?i)<EventRecordID>({event_id}[^<]+)"
      "(?i)<Message>({event_name}[^:=<.]+)\\."
    ]
    DupFields = [
      "host->dest_host"
      "process_path->process_command_line"
    ]
    ParserVersion = "v1.0.0"
  

}
```