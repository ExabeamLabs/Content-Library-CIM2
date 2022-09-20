#### Parser Content
```Java
{
Name = opendj-ldap-kv-endpoint-login-uid
  Vendor = OpenDJ
  Product = OpenDJ LDAP
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """uid=""", """ REQ conn=""", """op=""", """msgID=""" ]
  Fields = [
    """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]""",
    """conn=({connection_id}\d+)""",
    """uid=({user_uid}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```