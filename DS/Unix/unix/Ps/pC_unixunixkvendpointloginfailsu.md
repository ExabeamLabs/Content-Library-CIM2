#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-fail-su"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
""" su: pam_unix(su:auth)"""
"""authentication failure;"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+su:"""
"""\Wruser=({account}[^\s]+)"""
"""\Wuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""({result}failure)"""
  ]
  ParserVersion = "v1.0.0"


}
```