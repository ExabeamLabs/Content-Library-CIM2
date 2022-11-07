#### Parser Content
```Java
{
Name = opendj-ldap-kv-endpoint-login-connectconn
  Vendor = OpenDJ
  Product = OpenDJ LDAP
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """from=""", """to=""", """] CONNECT conn=""", """protocol=LDAP""" ]
  Fields = [
    """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]""",
    """conn=({connection_id}\d+)""",
    """from=({src_ip}[A-Fa-f:\d.]+)(:({src_port}\d+))""",
    """to=({dest_ip}[A-Fa-f:\d.]+)(:({dest_port}\d+))""",
    """protocol=({auth_method}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```