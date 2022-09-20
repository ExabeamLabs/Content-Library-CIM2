#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  Conditions = [ """Symantec|DLP""","""POLICY=""" ]
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """OCCURRED_ON=({time}\w+\s+\d+,\s*\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
    """({host}\S+)\s+\|?Symantec\|DLP""",
    """INCIDENT=({alert_id}\d+)\|""",
    """\|\s*POLICY=({alert_name}[^\|]+)""",
    """\|\s*SEVERITY=({alert_severity}[^\|]+)""",
    """\|\s*PROTOCOL=({protocol}[^\|]+)""",
    """\|\s*BLOCKED=(None|({action}[^\|]+))\|""",
    """\|\s*SENDER=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\|\s*ENDPOINT_USERNAME=(N\/A|(({domain}[^\s\\\|@]+)\\+)?({user}[^\s\\\|@]+))\|""",
    """\|\s*SENDER=(N\/A|({email_address}[^\\\s\|@]+@[^\\\s\|]+))\|""",
    """\|\s*RECIPIENTS=+(N\/A|({target}[^\|]+))""",
    """\|\s*SUBJECT=+\s*(N\/A|({email_subject}[^\|]+?))\s*\|""",
    """\|\s*ATTACHMENTS=({file_path}(({file_dir}[^"\|]+)?[\\\/]+)?({file_name}[^\|"]+?))\s*(\||$|")"""
  ]
  DupFields = [ "email_subject->additional_info" , "target->email_recipients"]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "protocol->dlpProtocol", "action->dlpActionTaken"]
    NameTemplate = """Symantec DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]

}
```