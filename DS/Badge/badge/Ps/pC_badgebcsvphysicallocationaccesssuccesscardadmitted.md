#### Parser Content
```Java
{
Name = badge-b-csv-physical-location-access-success-cardadmitted
    Vendor = Badge
    Product = Badge
    TimeFormat = "yyyy-MM-dd HH:mm:ss a"
    Conditions = [""",Card Admitted,"""]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d+:\d+:\d+ (am|AM|PM|pm))""",
      """({action}Admitted),"""
    ]
    ParserVersion = "v1.0.0"
  

}
```