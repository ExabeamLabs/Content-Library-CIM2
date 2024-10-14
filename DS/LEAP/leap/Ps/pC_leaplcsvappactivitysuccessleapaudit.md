#### Parser Content
```Java
{
Name = "leap-l-csv-app-activity-success-leapaudit"
Vendor = "LEAP"
Product = "LEAP"
TimeFormat = "yyyyMMdd:HH.mm.ss"
Conditions = [
""",LEAPAUDIT,"""
]
Fields = [
"""({location_country}\w+),({app_code}({app}LEAPS)[^,]*),LEAPAUDIT,({time}[^,]+),({user}[\w\.\-\!\#\^\~]{1,40}\$?),(NULL|null|({url}[^,]+)),(NULL|null|(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}[^,]+))),({object}[^,]+),"*({operation}.+?)\s*"*,({field_name}.+?),((("(.+?)")|(.+?)),){2}({primary_key}.+?),({secondary_key}.+?),(?:[^,]+,){2}("({additional_info}[^"]+)"|({=additional_info}[^,]+))(,"*({resource}.+?)"*\s*$)?"""
]
ParserVersion = "v1.0.0"


}
```