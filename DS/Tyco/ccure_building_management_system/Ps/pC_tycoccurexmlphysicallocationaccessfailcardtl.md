#### Parser Content
```Java
{
Name = "tyco-ccure-xml-physical-location-access-fail-card-tl"
    Vendor = "Tyco"
    Product = "CCURE Building Management System"
    ParserVersion = "v1.0.0"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [
      "<journallogmessagetype>"
      "<operatorname>ccure<"
      "<messagetext>"
      "<primaryobjectname>"
    ]
    Fields = [
      "(?i)<MessageLocalDateTime>({time}\\d+\\/\\d+\\/\\d+\\s+\\d+:\\d+:\\d+\\s+(AM|PM|am|pm))"
      "(?i)<JournalLogMessageType>({result}[^<]+)"
      "(?i)<MessageText>[^<]*?\\(Card:\\s*({badge_id}[^\\)]+)"
      "(?i)<PrimaryObjectName>({last_name}[^<,]+),\\s*({first_name}[^<,]+)"
      "(?i)<SecondaryObjectName>({location_door}[^<]+)"
    ]
  

}
```