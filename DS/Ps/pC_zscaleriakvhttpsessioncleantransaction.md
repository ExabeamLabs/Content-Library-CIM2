#### Parser Content
```Java
{
Name = "zscaler-ia-kv-http-session-cleantransaction"
Conditions = [
"""threatclass=Clean Transaction"""
"""bwthrottle="""
"""urlsupercategory="""
]
ParserVersion = "v1.0.0"

s-zscaler-web-activity.Fields}[
    """({time}\d\d\d\d-\d\d-\d\d\d\d:\d\d:\d\d)\s+reason=""",
  
}
```