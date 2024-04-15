#### Parser Content
```Java
{
Name = "leap-l-str-app-activity-success-leapshk"
Vendor = "LEAP"
Product = "LEAP"
TimeFormat = "yyyyMMdd:HH.mm.ss"
Conditions = [
"""|LEAPSHK|TUAUDIT|"""
]
Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
"""({location}\w+)\|({app_code}({app}LEAPS)[^\|]*)\|TUAUDIT\|({time}[^\|]+)\|({user}[^\|]+)\|[^\|]*\|\s*(?:|NULL|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}.+?))\s*\|({object}[^\|]+)\|[^\|]*\|({operation}[^\|]+)\|([^\|]*\|){6}({additional_info}[^\|]+)\|({resource}[^\|\s]+)\s*"""
]
ParserVersion = "v1.0.0"


}
```