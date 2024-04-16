#### Parser Content
```Java
{
Name = symantec-endpointprotection-csv-alert-trigger-success-sonaralloweddetection
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """,SONAR 検出を許可しました,""", """SHA2,会社名""" ]

symantec-alert-jp = {
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({alert_type}[^,]+)""",
    """,IP アドレス:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """,コンピュータ名:\s*({dest_host}[^,]+?)(,|\s*$)""",
    """,リスク名:\s*({alert_name}[^,]+?)(,|\s*$)""",
    """,実際の処理:\s*({action}[^,]+?)(,|\s*$)""",
    """,ユーザー:\s*({user}[\w\.\-]{1,40}\$?)(,|\s*$)""",
    """,カテゴリセット:\s*({category}[^,]+?)(,|\s*$)""",
    """,カテゴリの種類:\s*({threat_category}[^,]+?)(,|\s*$)""",
    """,アプリケーションハッシュ:\s*({hash_sha256}[^,]+?)(,|\s*$)""",
    """,件数:[^,]*,({file_path}({file_dir}[^,]*?[\\\/]+)?({file_name}[^\.\\\/]*?(\.({file_ext}\w+))?))\s*(,|\s*$)""",
  
}
```