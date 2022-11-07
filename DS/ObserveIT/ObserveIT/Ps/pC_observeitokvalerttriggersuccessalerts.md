#### Parser Content
```Java
{
Name = observeit-o-kv-alert-trigger-success-alerts
  Vendor = ObserveIT
  Product = ObserveIT
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """EventName =ObserveIT-Alerts;""" ]
  Fields = [
    """({host}\S+)\s+(\S+\s+){4}EventName =""",
    """\sAlertTime=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """\sOS=({os}[^;]+?)\s*(;|"*\s*$)""",
    """\sSeverity=({alert_severity}[^;]+?)\s*(;|"*\s*$)""",
    """\sRuleName =({alert_name}[^;]+?)\s*(;|"*\s*$)""",
    """\sAlertID=({alert_id}\d+)""",
    """\sAlertDetailsURL=({additional_info}[^;]+?)\s*(;|"*\s*$)""",
    """\sSessionID=({session_id}[^;]+?)\s*(;|"*\s*$)""",
    """\sServerName =({dest_host}[^;]+?)\s*(;|"*\s*$)""",
    """\sDomainName =({domain}[^;]+?)\s*(;|"*\s*$)""",
    """\sUserName =(?:n\/a|({user}[^;]+?))\s*(;|"*\s*$)""",
    """\sLoginName =({user}[^;]+?)\s*(;|"*\s*$)""",
    """\sClientName =(?:\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^;]+?))\s*(;|"*\s*$)""",
    """\sClientAddress=({src_ip}[a-fA-F\d.:]+)""",
    """\sApplicationName =({alert_type}[^;]+?)\s*(;|"*\s*$)""",
    """\sWindowTitle=({target}[^;]+?)\s*(;|"*\s*$)""",
    """\sProcessName =({process_path}[^;]+?)\s*(;|"*\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```