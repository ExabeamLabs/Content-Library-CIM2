#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-email-violationtriggers
  Vendor = Forcepoint
  Product = Forcepoint DLP
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """|Forcepoint|Forcepoint DLP|""", """violationTriggers="""", """CEF:""" ]
  Fields = [
    """eventTime="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """sourceHostname="({host}[\w\-.]+)"""",
    """application="({app}[^"]+)"""",
    """action="({action}[^"]+)"""",
    """direction="({direction}[^"]+)"""",
    """fileNames="(None|({email_attachments}({attachment}[^;"]+)[^"]*))"""",
    """fileSize="({bytes}\d+)"""",
    """incidentID="({alert_id}[^"]+)"""",
    """operationType="(None|({operation}[^"]+))"""",
    """rules="({alert_type}[^"]+?)\s*"""",
    """severity="({alert_severity}[^"]+)"""",
    """sourceEmail="({email_address}[^@"]+@[^\."]+\.[^"]+)""",
    """sourceIP="({src_ip}[A-Fa-f\d:.]+)"""",
    """sourceUsername="(({domain}[^\\"]+)\\)?({user}[^"]+)"""",
    """details="({additional_info}[^"]+?)\s*"""",
    """policies="({alert_name}[^"]+?)\s*"""",
  ]


}
```