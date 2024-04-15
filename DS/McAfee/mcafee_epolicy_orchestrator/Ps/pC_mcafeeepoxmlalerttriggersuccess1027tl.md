#### Parser Content
```Java
{
Name = "mcafee-epo-xml-alert-trigger-success-1027-tl"
    Vendor = "McAfee"
    Product = "McAfee ePolicy Orchestrator"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "epoevents"
      "<eventid>1027"
      "machinename>"
    ]
    Fields = [
      "(?i)\\d+\\s+({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)\\S*\\s+({host}[\\w\\-.]+)\\s+\\w+"
      "(?i)<MachineName>({src_host}[^<]+)<\\/MachineName>"
      "(?i)<IPAddress>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<\\/IPAddress>"
      "(?i)<UserName>({domain}[^\\\\]+)\\\\({user}[^<]+)<\\/UserName>"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)<Severity>({alert_severity}[^<]+)<\\/Severity>"
      "(?i)<FileName>({file_dir}[^<]+[\\\\\\/]+)({file_name}[^<]+?\\.({file_ext}[^<]+)?)"
      "(?i)<szVirusType>({alert_type}[^<]+)<\\/szVirusType>"
      "(?i)<MD5>({hash_md5}[^<]+)<\\/MD5>"
    ]
    DupFields = [
      "alert_type->alert_name"
    ]
  

}
```