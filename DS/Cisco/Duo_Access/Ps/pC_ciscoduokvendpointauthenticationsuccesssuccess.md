#### Parser Content
```Java
{
Name = cisco-duo-kv-endpoint-authentication-success-success
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """factor=""", """result=SUCCESS;""", """new_enrollment=""" ]
  Fields = [
    """\d\d:\d\d\s+({host}.+?)\s+(\S+\s+)*@\{\w+=""",
    """\Wdevice=\s*({device_name}[^;]+?)(?:;|\})""",
    """\Wintegration=\s*({integration}[^;]+?)(?:;|\})""",
    """\Wip=\s*(?:0\.0\.0\.0|({src_ip}[a-fA-F\d.:]+))""",
    """\Wresult=\s*({result}[^;]+?)(?:;|\})""",
    """timestamp=\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wusername=\s*({user}[^;]+?)(?:;|\})""",
    """\Wnew_enrollment=\s*({new_enrollment}[^;]+?)(?:;|\})""",
  ]
  ParserVersion = "v1.0.0"


}
```