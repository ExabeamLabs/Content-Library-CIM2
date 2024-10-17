#### Parser Content
```Java
{
Name = "checkpoint-sg-csv-vpn-logout-success-authcrypt"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "ddMMMyyyy HH:mm:ss"
Conditions = [
  """%CHKPNT-6-031085: authcrypt"""
  """disconnected from gateway"""
]
Fields = [
  """disconnected from gateway,([^,]*,){14}({time}[^,]+)"""
  """disconnected from gateway,([^,]*?,)({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```