#### Parser Content
```Java
{
Name = "ibm-sbi-kv-endpoint-login-success-usersessioncreated"
Vendor = "IBM"
Product = "Sterling B2B Integrator"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """[Login]: User session created for"""
  """sterling"""
]
Fields = [
  """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\+\d\d:\d\d)\s+\w+\s+sterling(?:\s-){3}"""
  """User session created for\s+({user_id}[^,]+)"""
  """({event_name}User session created)"""
]
ParserVersion = "v1.0.0"


}
```