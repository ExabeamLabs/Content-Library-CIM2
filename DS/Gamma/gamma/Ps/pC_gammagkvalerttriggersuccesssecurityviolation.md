#### Parser Content
```Java
{
Name = gamma-g-kv-alert-trigger-success-security-violation
  Vendor = Gamma
  Product = Gamma
  TimeFormat = "epoch_sec"
  ParserVersion = "v1.0.0"
  Conditions = [ """'violation_status': """, """'violation_category': """, """'violation_id':""", """'violation_event_timestamp':""" ]
  Fields = [
    """'violation_event_timestamp':\s+({time}\d{10})""",
    """'file_labels_map':[^:]+:\s+\['({event_name}[^']+)'""",
    """'dashboard_url':\s+'({additional_info}[^']+)'""",
    """'email_address':\s+'({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'""",
    """'slack_user_id':\s+'({user_id}[^']+)'""",
    """'active_directory_user_id':\s+'({user_id}[^']+)'""",
    """'email_address':\s+'({email_address}[^']+)'""",
    """'github_handle':\s+'({user_id}[^']+)'""",
    """'violation_category':\s+'({alert_type}[^']+)'""",
    """'app_name':\s+'({app}[^']+)'""",
    """'violation_id':\s+({alert_id}[^,\}]+)"""
  ]


}
```