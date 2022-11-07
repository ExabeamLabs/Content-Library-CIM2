#### Parser Content
```Java
{
Name = pingidentity-pi-kv-app-login-success-sso
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """event=SSO""", """status=success""",""" pfhost=""" ]
  Fields = [
    """\sip=(|({src_ip}[a-fA-F\d.:]+))\s\w+=""",
    """\spfhost=(|({host}[^=\s]+?))\s\w+=""",
    """\ssubject="(|(({email_address}[^"@\s]+@[^"@\s]+)|({user}[^"]+)))"""",
    """\sapp=(|({app}[^=]+?))\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```