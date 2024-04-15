#### Parser Content
```Java
{
Name = "tyco-ccure-xml-physical-location-access-objectname1-tl"
    Vendor = "Tyco"
    Product = "CCURE Building Management System"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [
      "objectname2"
      "objectname1"
      "<card>"
      "<statecode>"
    ]
    Fields = [
      "(?i)\"messageutc\\\":\\\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)\\\""
      "(?i)\"objectname1\\\":\\\"({last_name}[^,\\\"]+),\\s*({first_name}[^\\\"]+)\\\""
      "(?i)\"objectname2\\\":\\\"({location_door}[^\\\"]+)\\\""
      "(?i)<Card>({badge_id}.+?)</Card>"
      "(?i)<StateCode>({action}.+?)</StateCode>"
      "(?i)<Direction.*?>({direction}.+?)</Direction>"
    ]
    ParserVersion = "v1.0.0"
  

}
```