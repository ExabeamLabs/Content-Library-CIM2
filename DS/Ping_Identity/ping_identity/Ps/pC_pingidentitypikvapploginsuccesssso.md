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
    """\sip=(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s\w+=""",
    """\spfhost=(|({host}[^=\s]+?))\s\w+=""",
    """\ssubject="?(||(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\-\s"\\,;\|]+\.[^\]\s"\\,;\|\-]+))|(?:[^"]+?:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\-[^"]+)?"?(,|\s\w+=)""",
    """\sapp=(|({app}[^=]+?))\s\w+=""",
    """\sbrowser=\\"({user_agent}[^"]+?)\\?"""",
  ]
  ParserVersion = "v1.0.0"


}
```