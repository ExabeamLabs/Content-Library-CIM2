#### Parser Content
```Java
{
Name = rundeck-r-kv-app-notification-success-rundeckauditqa
  Vendor = Rundeck
  Product = Rundeck
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ RundeckAuditQA: """, """ - Evaluating Decision for: """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """Username:({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Group:({group_name}[^>]+)>""",
    """action<({operation}[^>]+)>""",
    """evaluations:\s*({additional_info}.+?)\s*$""",
    """authorized:\s+({result}[^,]+)""",
    """resource=\{kind=({object}[^\}]+)""",
    """application='({app}[^']+)'""",
    """({host}\S+) RundeckAuditQA: """,
  ]


}
```