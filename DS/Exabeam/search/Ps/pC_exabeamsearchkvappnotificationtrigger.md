#### Parser Content
```Java
{
Name = exabeam-search-kv-app-notification-trigger
  Vendor = Exabeam
  Product = Search
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  trigger_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """ Exabeam """, """ triggerTime="""", """ ruleDescription="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ({host}[\w.\-]+) ({app}Exabeam) """,
    """\striggerTime="({trigger_time}[^"]+)""",
    """\sruleName ="({rule}[^"]+)""",
    """\sruleDescription="({rule_description}[^"]+)""",
    # is_enabled is removed
    """\sseverity="({alert_severity}[^"]+)""",
    # realert is removed
    # num_matches is removed
    # query_delay is removed
  ]


}
```