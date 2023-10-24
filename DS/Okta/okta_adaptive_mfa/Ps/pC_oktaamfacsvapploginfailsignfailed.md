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
    """Sign-(i|I)n Failed.*?([^,]*,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Verification failed for user:\s*(({email_address}[^"@]+@[^"@]+)|({user}[\w\.\-]{1,40}\$?))"*,""",
    """([^,]*,){4}(({email_address}[^,@]+@[^,@]+)|({user}[\w\.\-]{1,40}\$?))""",
    """Sign-(i|I)n Failed\s*-\s*({failure_reason}[^:",]+)""",
    """([^,]*,){11}\/app\/({app}[^\/]+)""",
  ]
  DupFields = ["src_file_path->file_dir"]


}
```