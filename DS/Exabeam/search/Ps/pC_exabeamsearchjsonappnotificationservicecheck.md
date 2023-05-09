#### Parser Content
```Java
{
Name = exabeam-search-json-app-notification-servicecheck
    Vendor = Exabeam
    Product = Search
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = ["""exabeam-analytics-health""", """ServiceCheck"""]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"service"+: "+({service_name}[^"]+)"""",
      """"status"+: "+({result}[^"]+)"""",
    ]
  

}
```