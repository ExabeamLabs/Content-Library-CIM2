#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-activity-success-googleapismethodname
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  ParserVersion = "v1.0.0"
  Conditions = [ """googleapis.com""", """methodName""" ] 
  Fields = [
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"logName"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"log-name"+:\s*"+({event_category}[^",\s\[\{]+)"+""",
    """"status":.+"code":\s*({result_code}\d+)""",
    """"status":.+"message":\s*"?({failure_reason}[^

}
```