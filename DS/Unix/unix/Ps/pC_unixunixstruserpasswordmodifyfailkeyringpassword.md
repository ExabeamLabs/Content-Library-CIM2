#### Parser Content
```Java
{
Name = unix-unix-str-user-password-modify-fail-keyringpassword
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""couldn't update the""",
"""keyring password:"""
  ]
  Fields = [
"""({host}[\w.\-]+)\s+passwd(:|\[)"""
"""couldn't update the '({account}[^']+)"""
"""keyring password: ({failure_reason}.+?)\s*$"""
  ]
  
  DupFields = ["account->dest_user"]


}
```