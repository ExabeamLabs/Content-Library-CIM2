#### Parser Content
```Java
{
Name = "netwrix-auditor-xml-file-success-action-tl"
    Vendor = "Netwrix"
    Product = "Netwrix Auditor"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [
      "<eventrecordid>"
      " action : "
      " objecttype : "
      " what : "
    ]
    Fields = [
      "(?i)When\\s*:\\s*({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+Z)"
      "(?i)<Computer>({host}[\\w\\-.]+)"
      "(?i)>({event_code}\\d+)<\\/EventID>"
      "(?i)<EventRecordID>({event_id}.+?)<\\/EventRecordID>"
      "(?i)Action\\s*:\\s*({access}.+?)\\s*Message\\s*:"
      "(?i)Where\\s*:\\s*({dest_host}[\\w\\-.]+)"
      "(?i)ObjectType\\s*:\\s*({file_type}.+?)\\s*Who\\s*:"
      "(?i)Who\\s*:\\s*(({domain}[^\\\\\\s]+)\\\\+)?(system|({user}[^\\\\\\s]+))"
      "(?i)What\\s*:\\s*(|({src_file_path}({file_dir}[^\\\"]*?)[\\\\\\/]*({src_file_name}[^\\\\\\\"]+?(\\.({src_file_ext}[^\\\\\\.\\s\\\"]+))?)))\\s*When\\s*:"
      "(?i)Workstation\\s*:\\s*(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)\\s*Details\\s*:"
    ]
    ParserVersion = "v1.0.0"
  

}
```