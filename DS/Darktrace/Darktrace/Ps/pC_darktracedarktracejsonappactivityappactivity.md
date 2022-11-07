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
   """"+ip"+:"+\/*({src_ip}[^"]+)""",
   """"+method"+:"+({method}[^"]+)""",
   """"+status"+:({result_code}\d+)""",
   """"+description"+:"+({additional_info}[^"]+)"""
   ]


}
```