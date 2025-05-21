#### Parser Content
```Java
{
Name = cisco-duo-kv-endpoint-authentication-fail-failure
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """reason=""", """result=FAILURE;""", """new_enrollment=""" ]
  Fields = [
    """\d\d:\d\d\s+({host}.+?)\s+(\S+\s+)*@\{\w+=""",
    """\Wdevice=\s*({device_name}[^;]+?)(?:;|\})""",
    """\Wintegration=\s*({integration}[^;]+?)(?:;|\})""",
    """\Wip=\s*(?:0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\Wresult=\s*({result}[^;]+?)(?:;|\})""",
    """\Wreason=\s*({failure_reason}[^;]+?)(?:;|\})""",
    """timestamp=\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wusername=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:;|\})""",
    """\Wnew_enrollment=\s*({new_enrollment}[^;]+?)(?:;|\})""",
  ]
  ParserVersion = "v1.0.0"


}
```