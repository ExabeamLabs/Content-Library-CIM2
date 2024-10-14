#### Parser Content
```Java
{
Name = entrust-ie-str-app-activity-success-igsystem
  Vendor = Entrust
  Product = Entrust Identity Enterprise
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """] [IG.SYSTEM.""" ]
  Fields = [
    """\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])""",
# module is removed
    """\[IG.SYSTEM.[^\]]+?\] ({additional_info}.+)""",
    """for user (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\.?""",
  ]


}
```