#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-adminactivate
  Conditions = [ """ duo: """, """|admin_activate_duo_push|""", """": """" ]
  ParserVersion = "v1.0.0"

duo-app-activity-2 = {
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|({operation}[^\|]+)\|\{""",
    """\|({full_name}({first_name}[^\s"\|]+)\s({last_name}[^"\|]+))\|[^\|]*\|\{""",
    """"name":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[^\s"]+))"""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """"(phone|number)":\s*"({object}[^"]+)"""",
    """"role":\s*"({role}[^"]+)"""",
    """"status":\s*"({status}[^"]+)"""",
    """({app}duo)""",
  
}
```