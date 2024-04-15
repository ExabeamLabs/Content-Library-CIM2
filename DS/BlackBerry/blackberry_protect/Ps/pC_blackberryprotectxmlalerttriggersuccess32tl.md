#### Parser Content
```Java
{
Name = "blackberry-protect-xml-alert-trigger-success-32-tl"
    Vendor = "BlackBerry"
    Product = "BlackBerry Protect"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<event xmlns="
      "<provider name='cylancesvc'"
      ">32</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}.+?)<\\/Computer>"
      "(?i)({alert_name}A potentially malicious Active script was Detected)"
      "(?i)Device:\\s*({src_host}[\\w\\-.]+)"
      "(?i)MAC:\\s*({src_mac}[^\\s,;<]+)"
      "(?i)File path:\\s*(|({malware_url}.+?))\\s+Process Id:"
      "(?i)IP:\\s({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
    ]
    DupFields = [
      "alert_name->alert_type"
    ]
    ParserVersion = "v1.0.0"
  

}
```