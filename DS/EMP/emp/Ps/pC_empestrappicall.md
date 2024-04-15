#### Parser Content
```Java
{
Name = "emp-e-str-app-icall"
Vendor = "EMP"
Product = "EMP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""EMP-LOGS"""
"""|ICALL|"""
]
Fields = [
"""EMP-LOGS ([^\|]*\|)({location}[^\|]+)\|({app}[^\|]+)\|({host}[^\|]+)\|[^\|]*\|({user}[^\s\|]+)\|({operation}[^\|]+)\|({time}[^\|]+)\|(null|({object}[^\|]+))\|(null|({additional_info}[^\|]+))\|"""
]
DupFields = [
"app->app_code"
]
ParserVersion = "v1.0.0"


}
```