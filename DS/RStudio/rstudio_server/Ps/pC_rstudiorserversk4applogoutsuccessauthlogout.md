#### Parser Content
```Java
{
Name = rstudio-rserver-sk4-app-logout-success-authlogout
  Vendor = RStudio
  Product = RStudio Server
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """, auth_logout,""", """-rstudio-server/sessions""", """"logger.account":"""" ]
  Fields = [
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """({event_name}auth_logout)""",
    """message":"({additional_info}[^,]+),\s\\?"({user}[\w\.\-]{1,40}\$?)\\?""""
  ]


}
```