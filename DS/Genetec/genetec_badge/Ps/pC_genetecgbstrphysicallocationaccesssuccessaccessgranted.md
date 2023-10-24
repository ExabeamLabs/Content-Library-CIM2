#### Parser Content
```Java
{
Name = genetec-gb-str-physical-location-access-success-accessgranted
  Vendor = Genetec
  Product = Genetec Badge
  TimeFormat = "MM/dd/yyyy HH:mm:ss.SSSS a"
  Conditions = [""";AccessGranted;""","""Genetec;"""]
  Fields = [
    """({time}\d{1,2}\/\d{1,2}\/\d{4} \d{1,2}:\d{1,2}:\d{1,2}\.\d{1,4}\s((?i)am|pm));({result}[^;]+);([^;]*;){4}({location_door}[^;]+?)\:?\s*;""",
    """;AccessGranted\;([^\;]*\;)\s*(|None|EMS|EVS|UNKNOWN|[^\;]+\d+|(((?i)Dr|ER)\.?\s*)?((({first_name}\S+)\s+(((?i)Dr|ER)\.\s+)?({last_name}[^;\s]+?))|({full_name}[^;]+?)))\s*;"""
  ]
  DupFields = [ "result->event_name" ]
  ParserVersion = "v1.0.0"


}
```