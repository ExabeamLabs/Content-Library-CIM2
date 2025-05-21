#### Parser Content
```Java
{
Name = silverfort-s-cef-app-login-adminconsole
  Vendor = Silverfort
  Product = Silverfort Authentication Platform
  TimeFormat =["dd/MM/yyyy HH:mm:ss.SSS","MM/dd/yyyy HH:mm:ss.SSS"]
  Conditions = [ """ CEF:""", """|Silverfort|Admin Console|""", """|Authentication|Authentication request|""" ]
  Fields = [
    """\s+({host}[\w\-.]+)\s+CEF:""",
    """rt=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d.\d\d\d)""",
    """suser=(({email_address}[^@]+@({email_domain}[^\s]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\ssntdom=""",
    """sntdom=({domain}[^\s]+)""",
    """shost=(n\/a|({src_host}[^\s]+))""",
    """src=(n\/a|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """dhost=(n\/a|({dest_host}[^\s]+))""",
    """app=(n\/a|({app}[^\s]+))""",
    """cs2=({action}[^\s]+)""",
  ]
  ParserVersion = v1.0.0


}
```