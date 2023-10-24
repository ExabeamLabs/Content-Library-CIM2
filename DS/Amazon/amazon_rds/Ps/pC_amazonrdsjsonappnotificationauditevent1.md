#### Parser Content
```Java
{
Name = amazon-rds-json-app-notification-auditevent-1
  ParserVersion = "v1.0.0"
  Conditions = [ """]:WARNING: """,""""src-account-name":"Amazon RDS"""",""""event-name":"audit-event""""]

amazon-system-info = {
      Vendor = Amazon
      Product = Amazon RDS
      TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
      Fields = [
        """"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
        """\):({user}[\w\.\-]{1,40}\$?)@""",
        """table\s*\\?"({table_name}[^\\"]+)"""
      ]
    
}
```