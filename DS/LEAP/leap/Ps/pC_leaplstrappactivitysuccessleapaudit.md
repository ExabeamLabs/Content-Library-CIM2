#### Parser Content
```Java
{
Name = "leap-l-str-app-activity-success-leapaudit"
Vendor = "LEAP"
Product = "LEAP"
TimeFormat = "yyyyMMdd:HH.mm.ss"
Conditions = [
"""|LEAPAUDIT|"""
]
Fields = [
"""({location}\w+)\|({app_code}({app}LEAPS)[^\|]*)\|LEAPAUDIT\|({time}\d{8}:\d\d\.\d\d\.\d\d)\|(|({user}[\w\.\-]{1,40}\$?))\|([^\|]*\|){2}(|({object_name}[^\|]+))\|(|({field_name}[^\|]+))\|(|({operation}[^\|]+))\|(|({additional_info}[^\|]*\|[^\|]*))\|(|({primary_key}[^\|]+))\|\s*(|({secondary_key}[^\|]+))\s*\|"""
]
ParserVersion = "v1.0.0"


}
```