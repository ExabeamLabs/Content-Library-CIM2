#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-smtp-1
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """Policy_Violated=""", """Protocol="SMTP"""", """Subject=""", """Blocked=""" ]
    Fields = [
      """(\w+ \d+ \d\d:\d\d:\d\d)\s+({host}[^\s\.]+)\S* ID="({alert_id}\d+)""",
      """\sPolicy_Violated="({alert_name}[^"]+)""",
      """\sProtocol="({protocol}[^"]+)""",
      """\sRecipient="({target}[^"]*)""",
      """\sSender="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """\sSeverity=\s*"({alert_severity}[^"]+)""",
      """\sSubject="({additional_info}[^"]+)""",
      """\sBlocked="({action}[^"]+)"""
    ]
    DupFields = [ "protocol->alert_type" ]
    ParserVersion = "v1.0.0"
  

}
```