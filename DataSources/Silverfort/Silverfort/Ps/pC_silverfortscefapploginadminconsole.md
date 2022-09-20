#### Parser Content
```Java
{
Name = silverfort-s-cef-app-login-adminconsole
  Vendor = Silverfort
  Product = Silverfort
  TimeFormat ="dd/MM/yyyy HH:mm:ss.SSS"
  Conditions = [ """ CEF:""", """|Silverfort|Admin Console|""", """|Authentication|Authentication request|""" ]
  Fields = [
    """\s+({host}[\w\-.]+)\s+CEF:""",
    """rt=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d.\d\d\d)""",
    """suser=(({email_address}[^@]+@({email_domain}[^\s]+))|({user}.+?))\ssntdom=""",
    """sntdom=({domain}[^\s]+)""",
    """shost=(n\/a|({src_host}[^\s]+))""",
    """src=(n\/a|({src_ip}[a-fA-F\d\.:]+))""",
    """dhost=(n\/a|({dest_host}[^\s]+))""",
    """app=(n\/a|({app}[^\s]+))""",
    """cs2=({action}[^\s]+)""",
  ]
  ParserVersion = v1.0.0


}
```