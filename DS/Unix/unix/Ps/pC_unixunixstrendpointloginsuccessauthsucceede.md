#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-login-success-authsucceede
  ParserVersion = "v1.0.0"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" sshd["""
"""]: AD authentication succeeded for user"""
  ]
  Fields = [
"""AD authentication ({result}succeeded) for user ({user}[\w\.\-]{1,40}\$?)"""
  ]


}
```