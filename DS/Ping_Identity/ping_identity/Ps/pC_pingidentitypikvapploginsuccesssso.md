#### Parser Content
```Java
{
Name = pingidentity-pi-kv-app-login-success-sso
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """event=SSO""", """status=success""",""" pfhost=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
    """\sip=(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s\w+=""",
    """\spfhost=(|({host}[^=\s]+?))\s\w+=""",
    """\ssubject="(|(({email_address}[^"@\s]+@[^"@\s]+)|({user}[\w\.\-]{1,40}\$?)))"""",
    """\sapp=(|({app}[^=]+?))\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```