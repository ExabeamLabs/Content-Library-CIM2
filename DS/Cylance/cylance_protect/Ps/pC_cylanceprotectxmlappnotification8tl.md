#### Parser Content
```Java
{
Name = "cylance-protect-xml-app-notification-8-tl"
    Vendor = "Cylance"
    Product = "Cylance PROTECT"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<event xmlns="
      "<provider name='cylancesvc'"
      ">8</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}.+?)<\\/Computer>"
      "(?i)>({event_code}\\d+)<\\/EventID>"
      "(?i)<Provider Name ='({provider_name}[^']+)'"
      "(?i)<Message>({event_name}.+?)<\\/Message>"
      "(?i)Connected  Device:\\s*({src_host}[\\w\\-.]+)"
      "(?i)IP:\\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)MAC:\\s*({src_mac}[^\\s,;<]+)"
    ]
  

}
```