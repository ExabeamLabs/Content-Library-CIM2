#### Parser Content
```Java
{
Name = cisco-duo-kv-app-activity-success-userupdate
Product = Duo Access
Conditions = [
  """action=user_update;"""
  """object="""
  """timestamp="""
]
ParserVersion = "v1.0.0"

SSSSSSZ"]
  Fields = [
    """"ts"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\|({operation}[^\|]+)\|\{""",
    """\|({full_name}({first_name}[^\s"\|]+)\s({last_name}[^"\|]+))\|[^\|]*\|\{""",
    """"name":\s*"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """"(phone|number)":\s*"({object}[^"]+)"""",
    """"role":\s*"({role}[^"]+)"""",
    """"status":\s*"({status_msg}[^"]+)"""",
    """({app}duo)""",
  
}
```