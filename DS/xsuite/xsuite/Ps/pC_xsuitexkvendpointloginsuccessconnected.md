#### Parser Content
```Java
{
Name = "xsuite-x-kv-endpoint-login-success-connected"
Vendor = "xsuite"
Product = "xsuite"
TimeFormat = "yyyy-MM-dd HH:mm:ss z"
Conditions = [
  """xsuite["""
  """,connection,"""
  """ connected """
]
Fields = [
  """connected\sto\s({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})[:;]"""
  """connection,({dest_host}[\w.-]+),"""
  """({user_dn}CN\s*=\s*.+?)\",connection,"""
  """,\"?({user}[\w\.\-]{1,40}\$?)\"?,connection,"""
]
ParserVersion = "v1.0.0"


}
```