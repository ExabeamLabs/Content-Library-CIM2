#### Parser Content
```Java
{
Name = mcafee-es-csv-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "M/d/yy h:mm:ss a zzz"
  Conditions = [ """,Endpoint Security Platform,""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (am|AM|pm|PM) \w+),(?:|({src_host}[^,]+)),(?:|({alert_name}[^,]+)),(?:|({action}[^,]+)),[^,]*,Endpoint Security Platform,([^,]*,){2}(?:|({alert_type}[^,]+)),(?:|({additional_info}[^,]+)),(?:|({alert_severity}[^,]+)),(?:|({process_path}[^,]*?({process_name}[^,\\\/]+))),([^,]*,){2}\s*(?:,|({url}.+?))\s*($|\w+=)""",
  ]


}
```