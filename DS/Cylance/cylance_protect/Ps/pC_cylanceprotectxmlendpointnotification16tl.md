#### Parser Content
```Java
{
Name = "cylance-protect-xml-endpoint-notification-16-tl"
    Vendor = "Cylance"
    Product = "Cylance PROTECT"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<event xmlns="
      "<provider name='cylancesvc'"
      ">16</eventid>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)<Computer>({host}.+?)<\\/Computer>"
      "(?i)>({event_code}\\d+)<\\/EventID>"
      "(?i)<Provider Name ='({provider_name}[^']+)'"
      "(?i)<Message>({event_name}.+?)<\\/Message>"
    ]
  

}
```