#### Parser Content
```Java
{
Name = apache-guacamole-str-app-authentication-fail-authenticatethelockeduser
  ParserVersion = v1.0.0
  Vendor = Apache
  Product = Apache Guacamole
  TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
  Conditions = [ """realm.LockOutRealm.filterLockedAccounts""", """An attempt was made to authenticate the locked user ["""]
  Fields = [
    """({time}\d\d-\w\w\w-\d\d\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_name}An attempt was made to authenticate the locked user) \[({user}[^\]]+?)\]"""
    ]


}
```