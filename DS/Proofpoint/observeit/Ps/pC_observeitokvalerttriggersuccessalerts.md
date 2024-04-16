#### Parser Content
```Java
{
Name = observeit-o-kv-alert-trigger-success-alerts
  Vendor = Proofpoint
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
    """\sUserName =(?:n\/a|({user}[\w\.\-]{1,40}\$?))\s*(;|"*\s*$)""",
    """\sLoginName =({user}[\w\.\-]{1,40}\$?)\s*(;|"*\s*$)""",
    """\sClientName =(?:\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^;]+?))\s*(;|"*\s*$)""",
    """\sClientAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sApplicationName =({alert_type}[^;]+?)\s*(;|"*\s*$)""",
    """\sWindowTitle=({target}[^;]+?)\s*(;|"*\s*$)""",
    """\sProcessName =({process_path}[^;]+?)\s*(;|"*\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```