#### Parser Content
```Java
{
Name = zeek-z-json-email-send-success-smtp
Product = "Zeek"
Conditions = [
  """protocol"""
  """"smtp""""
  """"zeek""""
  """type"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

json-zeek-activity.Fields}[
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
  
}
```