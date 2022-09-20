#### Parser Content
```Java
{
Name = darktrace-darktrace-json-app-logout-success-endpointlogout
 Product = Darktrace
 Vendor = Darktrace
 ParserVersion = "v1.0.0"
 TimeFormat ="yyyy-MM-dd HH:mm:ss"
 Conditions =[ """endpoint":"/logout""", """description":"Logout""", """method":"GET""" ]
 Fields =[
   """"+username"+:"+({user}[^"]+)""",
   """"+endpoint"+:"+\/*({event_name}[^"]+)""",
   """"+ip"+:"+\/*({src_ip}[^"]+)""",
   """"+method"+:"+({method}[^"]+)""",
   """"+status"+:({result_code}\d+)""",
   """"+description"+:"+({additional_info}[^"]+)"""
   ]


}
```