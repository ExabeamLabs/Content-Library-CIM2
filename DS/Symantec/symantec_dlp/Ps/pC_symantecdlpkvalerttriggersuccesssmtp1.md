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
      """\sSender="({email_address}[^"]+)""",
      """\sSeverity="({alert_severity}[^"]+)""",
      """\sSubject="({additional_info}[^"]+)""",
      """\sBlocked="({action}[^"]+)"""
    ]
    DupFields = [ "protocol->alert_type", "email_address->src_email_address"]
    ParserVersion = "v1.0.0"
  

}
```