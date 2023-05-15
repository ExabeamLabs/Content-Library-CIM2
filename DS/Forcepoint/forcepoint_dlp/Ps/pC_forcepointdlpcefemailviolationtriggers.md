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
    """sourceIP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """sourceUsername="(({domain}[^\\"]+)\\)?({user}[^"]+)"""",
    """details="({additional_info}[^"]+?)\s*"""",
    """policies="({alert_name}[^"]+?)\s*"""",
  ]


}
```