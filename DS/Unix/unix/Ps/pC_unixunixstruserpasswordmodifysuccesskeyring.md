#### Parser Content
```Java
{
Name = unix-unix-str-user-password-modify-success-keyring
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
"""couldn't change password for""",
"""keyring:"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
"""({host}[\w.\-]+)\s+passwd:""",
"""couldn't change password for '({account}[^']+)""",
  ]


}
```