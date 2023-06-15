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
   """"+ip"+:"+\/*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """"+status"+:({result_code}\d+)""",
   """"+description"+:"+({additional_info}[^"]+)"""
   ]


}
```