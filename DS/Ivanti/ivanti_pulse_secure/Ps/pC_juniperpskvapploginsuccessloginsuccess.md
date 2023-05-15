#### Parser Content
```Java
{
Name = juniper-ps-kv-app-login-success-loginsuccess
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"AUT22670:""", """Login succeeded for""" ]
  Fields = [
    """\sfw=({host}[\w\-\.]+)""",
    """\w+\s*\d+\s*\d\d:\d\d:\d\d\s+({host}[\w.\-]+)\s*\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d""",
    """\stime="+({time}\d+-\d+-\d+ \d+:\d+:\d+).+?user""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """user=({user}.+?)\s+realm=""",
    """realm="+({app}[^"]+)""",
    """agent="+({user_agent}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```