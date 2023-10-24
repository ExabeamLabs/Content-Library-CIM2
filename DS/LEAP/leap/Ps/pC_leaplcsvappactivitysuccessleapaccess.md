#### Parser Content
```Java
{
Name = "leap-l-csv-app-activity-success-leapaccess"
Vendor = "LEAP"
Product = "LEAP"
TimeFormat = "yyyyMMdd:HH.mm.ss"
Conditions = [
""",LEAPACCESS,"""
]
Fields = [
"""({location_country}\w+),({app_code}({app}LEAPS)[^,]*),LEAPACCESS,({time}[^,]+),({user}[\w\.\-]{1,40}\$?),({url}[^,]+),\s*(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^,]+?))\s*,(NULL|null|({object}[^,]+?))\s*,(NULL|null|({field_name}[^,]+?))\s*,\s*"*({operation}[^,]+?)\s*"*,(?:[^,]+,){2}\s*(NULL|null|({primary_key}[^,]+?)),\s*(NULL|null|({secondary_key}[^,]+?)),(?:[^,]*,){2}\s*"+({additional_info}[^"]+?)"+(,\s*"(NULL|null|({resource}[^"]+)))?"""
]
ParserVersion ="v1.0.0"


}
```