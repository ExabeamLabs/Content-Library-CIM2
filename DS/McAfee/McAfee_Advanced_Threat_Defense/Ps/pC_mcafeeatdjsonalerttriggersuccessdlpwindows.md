#### Parser Content
```Java
{
Name = mcafee-atd-json-alert-trigger-success-dlpwindows
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Advanced Threat Defense
  TimeFormat = "MMM dd, YYYY HH:mm:ss a"
  Conditions = ["""occurred_endpoint""" , """device_class_name""" , """DLP for Windows"""]
  Fields = [
    """"occurred_endpoint":"({time}\w+\s\d\d,\s\d\d\d\d\s\d+:\d\d:\d\d\s(am|AM|pm|PM))""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"incident_type":"({alert_type}[^"]+)"""",
    """"computer_ip":"({host}[^"]+)"""",
    """"computer_name":"({host}[^"]+)"""",
    """"device_friendly_name_":"({device_id}[^"]+)"""",
    """"actual_action":"({action}[^"]+)"""",
    """"total_content_size_kb":"({bytes}[\d.]+)"""",
    """total_content_size_({bytes_unit}[^"]+)":"\d""",
    """"user_name":"({user}[^"]+)"""",
    """"user_groups":"({additional_info}[^"]+)"""",
    """"incident_id":"({alert_id}[^"]+)"""",
    """"destination":"({target}[^"]+)"""",
    """"rules":"({alert_name}[^",]+)(,|")""",
    """"source_application_file_name":"(?:None|({process_path}[^"]+))""",
    """"evidence_file_path":"(?:None|\w+:\\+([^\\"]+\\+)+({file_name}[^"]+))"""",
    """"evidence_file_path":"(?:None|({file_path}[^"]+))"""",
  ]


}
```