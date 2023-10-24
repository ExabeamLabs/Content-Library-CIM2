#### Parser Content
```Java
{
Name = "leap-l-str-app-activity-success-leapaccess"
Vendor = "LEAP"
Product = "LEAP"
TimeFormat = "yyyyMMdd:HH.mm.ss"
Conditions = [
"""|LEAPACCESS|"""
]
Fields = [
"""({location}\w+)\|({app_code}({app}LEAPS)[^\|]*)\|LEAPACCESS\|({time}[^\|]+)\|({user}[\w\.\-]{1,40}\$?)\|({object}[^\|]+)\|\s*(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}.+?))\s*\|([^\|]*\|){2}({operation}[^\|]+)\|([^\|]*\|){4}(|({additional_info}.*?))\s*$"""
]
ParserVersion = "v1.0.0"


}
```