#### Parser Content
```Java
{
Name = dg-ndlp-kv-email-send-success-smtp
  Vendor = Digital Guardian
  Product = Digital Guardian Network DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """protocol="SMTP"""", """email_subject=""" ]
  Fields = [
    """timestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d \w+)"""",
    """\d\d:\d\d ({host}[^\s]+)\s+\d+\s+\d{4}\-\d\d\-\d\d""",
    """source="(?:\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """email_sender="(?:|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
    """email_recipients="({email_recipients}.+?)"""",
    """inspected_document="(?:|({file_name}.+?))"""",
    """inspected_document="(?:|({email_attachment}.+?))"""",
    """inspected_document="[^"]+\.({extension}[^\s"\/]+)""",
    """email_subject="({email_subject}.+?)"""",
    """({alert_type}SMTP)""",
    """source_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """destination_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """matched_policies_by_severity="({alert_severity}[^"]+)""",
    """matched_policies_by_severity="\w+:({alert_name}[^,;\/]+)""",
    """({direction}o)""",
    """action_taken="(?:|({result}[^"]+))""""
  ]
  ParserVersion = "v1.0.0"


}
```