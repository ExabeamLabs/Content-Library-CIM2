#### Parser Content
```Java
{
Name = "fastenterprises-gt-str-app-login-success-accesslogs"
Vendor = "Fast Enterprises"
Product = "Fast Enterprises GenTax"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""",WEB.GENTAX,"""
""",AccessLogs,"""
]
Fields = [
"""({app}WEB\.GENTAX),({event_category}AccessLogs)"""
""",AccessLogs,({category}[^,]+),({user_id}[^,]+),({user}[^,]+),({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
]
ParserVersion = "v1.0.0"


}
```