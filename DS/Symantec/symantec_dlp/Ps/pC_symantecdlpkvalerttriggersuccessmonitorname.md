#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-monitorname
   Vendor = Symantec
   Product = Symantec DLP
   TimeFormat = "MMM dd, yyyy HH:mm:ss"
   Conditions = [  """,incident_id=""", """,block=""", """,policy=""", """,monitor_name=""", """,subject="""   ]
   Fields = [
     """\w+\s*\d+\s*\d+:\d+:\d+\s+({host}[^\s]+)\s+application""",
     """occurred_on="+(({time}.+?)\s+(:?AM|PM|am|pm))""",
     """incident_id="+({alert_id}[^"]+)""",
     """subject="+({email_subject}.+?)\s*"""",
     """policy_rules="+({alert_type}[^"]+)""",
     """protocol="+({protocol}[^"]+)""",
     """severity="+({alert_severity}[^"]+)""",
     """(policy|Policy)="+({alert_name}[^"]+)""",
     """sender="+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|(WinNT:\/+)?({domain}[^\\\/]+)(\\|\/)({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+""",     
     """block="+({action}[^"]+)""",
     """recipients="+((({target}http.+?)"+)|({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)"+)""",
     """attachment="+({email_attachments}[^"]+)\s+""",
     """match_count="+({match_count}[^"]+)""",
  ]
  DupFields = [ "email_attachments->file_name"]
  ParserVersion = "v1.0.0"


}
```