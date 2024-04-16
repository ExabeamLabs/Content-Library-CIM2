#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  Conditions = [ """Symantec|DLP""","""POLICY=""" ]
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd, yyyy hh:mm:ss a","yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s*({host}[\w\-.]+)\s*""",
    """OCCURRED_ON=({time}\w+\s+\d+,\s*\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))""",
    """({host}\S+)\s+\|?Symantec\|DLP""",
    """INCIDENT=({alert_id}\d+)\|""",
    """\|\s*POLICY=({alert_name}[^\|]+)""",
    """\|\s*SEVERITY=({alert_severity}[^\|]+)""",
    """\|\s*PROTOCOL=({protocol}[^\|]+)""",
    """\|\s*BLOCKED=(None|({action}\w+))""",
    """\|\s*SENDER=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|\s*ENDPOINT_USERNAME=(N\/A|(({domain}[^\s\\\|@]+)\\+)?({user}[\w\.\-]{1,40}\$?))\|""",
    """\|\s*SENDER=(N\/A|({email_address}[^\\\s\|@]+@[^\\\s\|]+))\|""",
    """\|\s*RECIPIENTS=+(N\/A|({target}[^\|]+))""",
    """\|\s*SUBJECT=+\s*(N\/A|({email_subject}[^\|]+?))\s*\|""",
    """\|\s*ATTACHMENTS=({file_path}(({file_dir}[^"\|]+)?[\\\/]+)?({file_name}[^\|"]+?))\s*(\||$|")""",
    """"timestamp":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3}Z)\s*"""
  ]
  DupFields = [ "email_subject->additional_info" , "target->email_recipients", "email_address->src_email_address"]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "protocol->dlpProtocol", "action->dlpActionTaken"]
    NameTemplate = """Symantec DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]

}
```