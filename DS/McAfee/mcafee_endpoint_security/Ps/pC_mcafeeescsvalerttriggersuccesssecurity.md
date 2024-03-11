#### Parser Content
```Java
{
Name = mcafee-es-csv-alert-trigger-success-security
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "M/d/yy h:mm:ss a zzz"
    Conditions = [ """,McAfee Endpoint Security,""" ]
    Fields = [
      """({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (am|AM|pm|PM) \w+),(?:|({src_host}[^,]+)),(?:|({alert_name}[^,]+)),(?:|({action}[^,]+)),[^,]*,McAfee Endpoint Security,([^,]*,){2}(?:|({alert_type}[^,]+)),(?:|({additional_info}[^,]+)),(?:|({alert_severity}[^,]+)),(?:|({process_path}[^,]*?({process_name}[^,\\\/]+))),([^,]*,){2}\s*(?:,|({malware_url}.+?))\s*$""",
    ]
    ParserVersion = "v1.0.0"
  

}
```