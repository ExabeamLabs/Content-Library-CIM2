#### Parser Content
```Java
{
Name = absolute-siemconnector-cef-app-login-success-loggedin
  Vendor = Absolute
  Product = Absolute DDS
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """AbsoluteSIEMConnector""", """eventType="UserLogin"""", """actorType="User"""", """actorName =""", """verb="LoggedIn"""" ]
  Fields = [
    """date="({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2}\s\w{3})""",
    """\s({host}[\w\-.]+)\sAbsoluteSIEMConnector""",
    """({event_name}LoggedIn)""",
    """({operation}UserLogin)""",
    """actorName ="(({email_user}[^"@]+@[^".]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """objectProperties="({additional_info}.+?)"\s+\w+="""
   ]


}
```