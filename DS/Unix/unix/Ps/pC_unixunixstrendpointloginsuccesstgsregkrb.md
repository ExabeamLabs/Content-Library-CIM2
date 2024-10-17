#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-success-tgs-reg-krb"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "epoch_sec"
  Conditions = [
  """krb5kdc"""
  """TGS_REQ"""
  """: ISSUE:"""
  ]
  Fields = [
  """\sauthtime ({time}\d{10})"""
  """\w+ \d+ \d+:\d+:\d+ ({host}[^\s]+)"""
  """TGS_REQ .+? ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """},\s+(?:(host\/)({src_host}[^@\s]+)@({domain}[^\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({=domain}[^\s]+)) for ({kerberos_service_name}[^/]+)/({dest_host}[^@]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```