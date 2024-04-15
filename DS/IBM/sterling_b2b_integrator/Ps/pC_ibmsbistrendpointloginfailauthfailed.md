#### Parser Content
```Java
{
Name = "ibm-sbi-str-endpoint-login-fail-authfailed"
Vendor = "IBM"
Product = "Sterling B2B Integrator"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """failed in public key auth"""
  """sterling"""
]
Fields = [
  """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\+\d\d:\d\d)\s+\w+\s+sterling(?:\s-){3}"""
  """userToAuth\s+({user_id}[^:]+)"""
  """({event_name}Failed login)"""
]
ParserVersion = "v1.0.0"


}
```