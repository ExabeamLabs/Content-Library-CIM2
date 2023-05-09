#### Parser Content
```Java
{
Name = ibm-sbi-csv-app-notification-success-nologinfailures
  Vendor = IBM
  Product = Sterling B2B Integrator
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """SecurityManager""", """No login failures for the user""",  """sterling"""]
  Fields = [
    """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\+\d\d:\d\d)\s+\w+\s+sterling(?:\s-){3}""",
    """SecurityManager No login failures for the user:({user_id}[^,]+)""",
    """({event_name}No login failures)""",
  ]
  ParserVersion = "v1.0.0"


}
```