#### Parser Content
```Java
{
Name = "ibm-sbi-str-endpoint-login-fail-loginfailure"
Vendor = "IBM"
Product = "Sterling B2B Integrator"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """[Login] Login failure for user"""
  """sterling"""
]
Fields = [
  """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\+\d\d:\d\d)\s+\w+\s+sterling(?:\s-){3}"""
  """Login failure for :({user_id}[^:]+)"""
  """Login failure for :[^:]+:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({event_name}Failed login)"""
]
ParserVersion = "v1.0.0"


}
```