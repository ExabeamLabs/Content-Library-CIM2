#### Parser Content
```Java
{
Name = ibm-sbi-str-app-authentication-fail-authorizationfailed
  Vendor = IBM
  Product = Sterling B2B Integrator
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """SecurityManager""", """authorization FAILED""",  """sterling"""]
  Fields = [
    """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\+\d\d:\d\d)\s+\w+\s+sterling(?:\s-){3}""",
    """SecurityManager\s+user:({user_id}[^\s]+)""",
    """SecurityManager\s+user:[^\s]+\s+({description}[^,]+)""",
    """({event_name}(?i)authorization FAILED)""",
  ]
  ParserVersion = "v1.0.0"


}
```