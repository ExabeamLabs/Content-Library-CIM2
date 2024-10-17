#### Parser Content
```Java
{
Name = symantec-endpointprotection-csv-alert-trigger-success-threatnum
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """スキャンが開始されました""", """,スキャン ID:""" ]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d),スキャン ID:""",
      """スキャン ID:\s*({alert_id}\d+)""",
      """ユーザー 1:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """IP アドレス:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """コンピュータ:\s*({src_host}[\w\-.]+)""",
      """,({alert_name}[^,]+),スキャン 完了:""",
      """グループ:\s*({malware_url}[^,]+)""",
      """脅威:\s*({threat_num}[^,]+)""",
      """感染:\s*({infection_num}[^,]+)""",
    ]
    DupFields = [ "alert_name->alert_type" ]
  

}
```