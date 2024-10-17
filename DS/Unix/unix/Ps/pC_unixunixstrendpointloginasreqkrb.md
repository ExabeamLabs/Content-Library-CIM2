#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-as-req-krb"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "epoch_sec"
  Conditions = [
  """krb5kdc"""
  """AS_REQ"""
  ]
  Fields = [
  """authtime ({time}\d{10}),"""
  """\w+ \d+ \d+:\d+:\d+ ({host}[^\s]+)"""
  """AS_REQ .+? ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):\s+({action}[^:]+)"""
  """AS_REQ.+?(,|:)\s+(?:(host\/)({src_host}[^@\s]+)@({domain}[^\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?@({=domain}[^\s]+)) for ({kerberos_service_name}[^/]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```