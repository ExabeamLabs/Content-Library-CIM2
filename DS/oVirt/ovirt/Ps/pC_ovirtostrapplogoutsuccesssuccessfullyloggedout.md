#### Parser Content
```Java
{
Name = ovirt-o-str-app-logout-success-successfullyloggedout
  Vendor = oVirt
  Product = oVirt
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """INFO""", """ovirt""", """successfully logged out""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """User (?:({email_address}[^\s@]+@[^\s@]+)\S*|({user}[^\s]+)) successfully logged out""",
  ]


}
```