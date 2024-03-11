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
    ""","(|[- ]+|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)",((\s*"([^"]|"")+")\s*,|[^",]+?,|\s*,){9}\s*"Message 18019:""",
    """"Message 18019:\s*User\s+({user}.+?)\s+logged in successfully""",
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = v1.0.0


}
```