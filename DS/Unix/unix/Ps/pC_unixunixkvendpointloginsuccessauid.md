#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-success-auid"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """type=LOGIN"""
    """auid"""
  ]
  Fields = [
    """msg=audit\(({time}\d{10})"""
    """,({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})"""
    """pid=({process_id}\d+)"""
    """\suid=({user_id}\d+)"""
    """\sses=({session_id}\d+)"""
    """\sauid=({account_id}\d+)"""
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s"""
    """type=({login_type_text}[^\s]+)"""
  ]
  DupFields = ["login_type_text->operation_type"]
  ParserVersion = "v1.0.0"


}
```