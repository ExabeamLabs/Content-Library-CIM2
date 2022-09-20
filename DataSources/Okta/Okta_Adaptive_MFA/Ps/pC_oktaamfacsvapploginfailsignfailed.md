#### Parser Content
```Java
{
Name = okta-amfa-csv-app-login-fail-signfailed
  ParserVersion = v1.0.0
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,Sign-""", """n Failed """]
  Fields = [
    """([^,]*,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """Sign-(i|I)n Failed.*?([^,]*,){3}({src_ip}[^,]+)""",
    """Verification failed for user:\s*(({email_address}[^"@]+@[^"@]+)|({user}[^"]+))"*,""",
    """([^,]*,){4}(({email_address}[^,@]+@[^,@]+)|({user}[^,]+))""",
    """Sign-(i|I)n Failed\s*-\s*({failure_reason}[^:",]+)""",
    """([^,]*,){11}\/app\/({app}[^\/]+)""",
  ]
  DupFields = ["src_file_path->file_dir"]


}
```