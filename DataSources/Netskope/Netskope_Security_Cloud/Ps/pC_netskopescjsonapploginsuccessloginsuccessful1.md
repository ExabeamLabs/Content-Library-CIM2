#### Parser Content
```Java
{
Name = netskope-sc-json-app-login-success-loginsuccessful-1
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """"type": "admin_audit_logs"""", """"audit_log_event":""", """Login Successful"""" ]
  Fields = [
    """"timestamp": ({time}\d+)""",
    """"user": "(?![^\s]+@[^\s]+)({user}[^"\s]+)"""",
    """"user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""",
  ]
  ParserVersion = "v1.0.0"


}
```