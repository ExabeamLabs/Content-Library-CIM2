#### Parser Content
```Java
{
Name = xceedium-x-csv-app-login-success-loggedin
  Vendor = Xceedium
  Product = Xceedium
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """Message 18019:""", """logged in successfully""" ]
  Fields = [
    """"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"+\s*,""",
    ""","(|[- ]+|({src_ip}\S+?))",((\s*"([^"]|"")+")\s*,|[^",]+?,|\s*,){9}\s*"Message 18019:""",
    """"Message 18019:\s*User\s+({user}.+?)\s+logged in successfully""",
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = v1.0.0


}
```