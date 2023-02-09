#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-name-modify-4781
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """The name of an account was changed""", """4781""" ]
  Fields = [
    """({event_name}The name of an account was changed)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4781)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}.+?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Target Account:\s*(|-|({dest_user}.+?))\s*Security ID:\s*(|-|({dest_user_sid}.+?))\s*Account Domain:\s*(|-|({dest_domain}.+?))\s*Old Account Name:\s*(|-|({old_user_name}.+?))\s*New Account Name:\s*(|-|({new_user_name}.+?))\s*Additional Information:\s*(|-|({additional_info}.+?))\s*Privileges:\s*(|-|({privileges}.+?))\s*($|<)""",
  ]
  DupFields = [ "host-> dest_host" ]


}
```