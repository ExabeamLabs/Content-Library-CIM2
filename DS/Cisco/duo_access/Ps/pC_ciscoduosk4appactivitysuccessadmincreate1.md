#### Parser Content
```Java
{
Name = cisco-duo-sk4-app-activity-success-admincreate-1
  Conditions = [ """ duo: """, """|admin_create|""", """": """" ]
  ParserVersion = "v1.0.0"

duo-app-activity-2 = {
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|({operation}[^\|]+)\|\{""",
    """\|({full_name}({first_name}[^\s"\|]+)\s({last_name}[^"\|]+))\|[^\|]*\|\{""",
    """"name":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-]{1,40}\$?))"""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """"(phone|number)":\s*"({object}[^"]+)"""",
    """"role":\s*"({role}[^"]+)"""",
    """"status":\s*"({status}[^"]+)"""",
    """({app}duo)""",
  
}
```