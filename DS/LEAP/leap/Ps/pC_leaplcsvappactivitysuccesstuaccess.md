#### Parser Content
```Java
{
Name = "leap-l-csv-app-activity-success-tuaccess"
Vendor = "LEAP"
Product = "LEAP"
TimeFormat = "yyyyMMdd:HH.mm.ss"
Conditions = [
""",LEAPSHK,TUACCESS,"""
]
Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
"""({location}\w+),({app_code}({app}LEAPS)[^,]*),TUACCESS,({time}[^,]+),({user}[^,]+),({additional_info}[^,]+),\s*(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}.+?))\s*,([^,]*,){2}({operation}[^,]+),([^,]*,){4}(|({object}[^,]*?))\s*,(|({resource}[^,]*?))\s*,"""
]
ParserVersion = "v1.0.0"


}
```