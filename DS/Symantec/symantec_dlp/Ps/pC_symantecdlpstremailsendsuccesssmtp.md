#### Parser Content
```Java
{
Name = symantec-dlp-str-email-send-success-smtp
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy/MM/dd H:mm:ss"
    Conditions = [ """対象の種類:SMTP""", """送信者:""", """受信者:""", """報告日:""" ]
    Fields = [
      """報告日:({time}\d\d\d\d/\d\d/\d\d \d+:\d\d:\d\d)""",
      """({host}[\w.\-]+)\s+URL:""",
      """インシデント ID:({alert_id}\d+)""",
      """ポリシールール:({alert_type}[^,]+)""",
      """ポリシー名:({alert_name}[^,]+)""",
      """件名:\s*({email_subject}[^,]+?)\s*,""",
      """遮断:({action}[^,]+)""",
      """受信者:({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """重大度:({alert_severity}[^,]+)""",
      """送信者:({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """添付ファイル名:\s*(N/A|({email_attachments}(Unknown|({email_attachment}[^,@\s]+))[^,]*?))\s*,""",
      """一致件数:\s*({number_of_violations}\d+)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```