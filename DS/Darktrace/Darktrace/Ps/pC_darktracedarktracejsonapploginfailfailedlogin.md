#### Parser Content
```Java
{
Name = darktrace-darktrace-json-app-login-fail-failedlogin
 ParserVersion = v1.0.0
 Product = Darktrace
 Vendor = Darktrace
 TimeFormat ="yyyy-MM-dd HH:mm:ss"
 Conditions =[ """endpoint":"/login""", """description":"""", """Failed login""", """method":"POST""" ]
 Fields =[
   """"+username"+:"+({user}[^"]+)""",
   """"+endpoint"+:"+\/*({operation}[^"]+)""",
   """"+method"+:"+({method}[^"]+)"""
   """"+ip"+:"+\/*({src_ip}[^"]+)""",
   """"+status"+:({failure_code}\d+)""",
   """"+description"+:"+({additional_info}[^"]+)"""
   ]


}
```