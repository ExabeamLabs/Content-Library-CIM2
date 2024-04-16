#### Parser Content
```Java
{
Name = oracle-am-str-app-login-authn
  Vendor = Oracle
  Product = Oracle Access Management
  TimeFormat = "MM/dd/yyyy HH:mm:ss z"
  Conditions = [ """| AUTHN_""", """OAM_LOGIN |""", """|uid=""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w+)\s*\|""",
    """([^\|]*\|){1}\s*({result}[^\|]+?)\s*\|""",
    """([^\|]*\|){2}\s*({host}[^\|]+?)\s*\|""",
    """([^\|]*\|){3}\s*({additional_info}[^\|]+?)\s*\|""",
    """([^\|]*\|){5}\s*({auth_method}[^\|]+?)\s*\|""",
    """([^\|]*\|){6}\s*({app}[^\|]+?)_LOGIN\s*\|""",
    """([^\|]*\|){7}\s*uid=({user}[\w\.\-]{1,40}\$?)""",
  ]
  ParserVersion = v1.0.0


}
```