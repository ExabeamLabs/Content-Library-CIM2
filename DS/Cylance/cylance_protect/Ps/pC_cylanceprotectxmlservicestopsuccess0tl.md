#### Parser Content
```Java
{
Name = "cylance-protect-xml-service-stop-success-0-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Cylance"
    Product = "Cylance PROTECT"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<event xmlns="
      "<provider name='cylancesvc'"
      ">0</eventid>"
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