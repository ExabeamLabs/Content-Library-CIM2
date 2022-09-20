#### Parser Content
```Java
{
Name = cisco-duo-csv-app-login-fail-failure
  Vendor = Cisco
  Product = Duo Access Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ ""","FAILURE",""""]
  Fields = [
    """FAILURE","({user}[^"]+)"""",
    """"({failure_reason}[^"]+)","FAILURE",""",
    """"\d{10}",(("[^"]+")?,)"(?:n\/a|({auth_method}[^"]+))"""",
    """"\d{10}",(("[^"]+")?,){2}"({app}[^"]+)"""",
    """"\d{10}",(("[^"]+")?,){3}"(?:0\.0\.0\.0|({src_ip}[^"]+))""""
  ]


}
```