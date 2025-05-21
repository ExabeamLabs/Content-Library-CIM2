#### Parser Content
```Java
{
Name = symantec-dlp-csv-alert-trigger-success-https
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy/MM/dd H:mm:ss"
    Conditions = [ """対象の種類:HTTPS""", """ポリシー名:""", """報告日:""" ]
    Fields = [
      """報告日:({time}\d\d\d\d/\d\d/\d\d \d+:\d\d:\d\d)""",
      """({host}[\w.\-]+)\s+URL:""",
      """インシデント ID:({alert_id}\d+)""",
      """ポリシールール:({alert_type}[^,]+)""",
      """ポリシー名:({alert_name}[^,]+)""",
      """遮断:({action}[^,]+)""",
      """受信者:({target}[^,]+)""",
      """重大度:({alert_severity}[^,]+)""",
      """送信者:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """添付ファイル名:(N/A|({additional_info}[^,]+?))\s*(,|$)""",
      """一致件数:\s*({number_of_violations}\d+)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```