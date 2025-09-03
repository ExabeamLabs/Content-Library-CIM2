#### Parser Content
```Java
{
Name = kemp-loadmaster-str-app-notification-smtpalertsuccessfullysent
  Vendor = Kemp
  Product =  Kemp LoadMaster
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """mailer: """, """SMTP alert successfully sent.""" ]
  Fields = [
    """mailer:\s+({event_name}.+?)\.\s+$""",
    """({event_category}mailer)"""
  ]


}
```