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
   """"+username"+:"+({user}[\w\.\-]{1,40}\$?)""",
   """"+endpoint"+:"+\/*({event_name}[^"]+)""",
   """"+ip"+:"+\/*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """"+method"+:"+({method}[^"]+)""",
   """"+status"+:({result_code}\d+)""",
   """"+description"+:"+({additional_info}[^"]+)"""
   ]


}
```