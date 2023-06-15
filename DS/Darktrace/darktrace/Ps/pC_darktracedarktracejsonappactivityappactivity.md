#### Parser Content
```Java
{
Name = darktrace-darktrace-json-app-activity-appactivity
 ParserVersion = "v1.0.0"
 Product = Darktrace
 Vendor = Darktrace
 TimeFormat ="yyyy-MM-dd HH:mm:ss"
 Conditions =[ """endpoint":"""", """description":"""", """username":"""", """method":"""" ]
 Fields =[
   """"+username"+:"+({user}[^"]+)""",
   """"+endpoint"+:"+\/*({event_name}[^"]+)""",
   """"+ip"+:"+\/*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """"+method"+:"+({method}[^"]+)""",
   """"+status"+:({result_code}\d+)""",
   """"+description"+:"+({additional_info}[^"]+)"""
   ]


}
```