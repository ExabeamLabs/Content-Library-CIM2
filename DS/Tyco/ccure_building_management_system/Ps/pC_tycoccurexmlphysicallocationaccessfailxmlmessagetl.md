#### Parser Content
```Java
{
Name = "tyco-ccure-xml-physical-location-access-fail-xmlmessage-tl"
    Vendor = "Tyco"
    Product = "CCURE Building Management System"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "xmlmessage:"
      "messagetype: \"card"
      "primarypartitionname:"
    ]
    Fields = [
      "(?i)ServerUTC:\\s*\\\"({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)"
      "(?i)MessageType:\\s*\\\"({result}[^\\\"]+)"
      "(?i)<Direction>\\s*({direction}.+)\\s*</Direction>"
      "(?i)<Card>\\s*({badge_id}\\d+)\\s*</Card>"
      "(?i)<PrimaryObjectName>\\s*({last_name}[^,]+?),\\s*({first_name}.*?)\\s*</PrimaryObjectName>"
      "(?i)<SecondaryObjectName>\\s*({location_door}.+?)\\s*</SecondaryObjectName>"
      "(?i)PrimaryPartitionName:\\s*\\\"({user_city}[^\\\"]+)"
      "(?i)<AdmitCode>\\s*({result_reason}.+?)\\s*</AdmitCode>"
      "(?i)<RejectCode>\\s*({result_reason}.+?)\\s*</RejectCode>"
    ]
    ParserVersion = "v1.0.0"
  

}
```