#### Parser Content
```Java
{
Name = "microsoft-evsecurity-csv-file-success-560"
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """,560,""", """|NetApp Data ONTAP|""", """オブジェクト アクセス""" ]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),560,""",
      """({event_code}560)""",
      """オブジェクトの種類:\s+({file_type}[^\s]+)\s+""",
      """オブジェクト名:\s+({file_path}.+?)\s+ハンドル ID:""",
      """オブジェクト名:\s+.*\\({file_name}(?:[^\\:]+(?=\.))({file_ext}\.[^\\:\s]+)?|[^\\:\s]+)\s*ハンドル ID:""",
      """オブジェクト名:\s+({file_dir}.+?)\\(?:[^\\]+?)\s*ハンドル ID:""",
      """プライマリ ユーザー名:\s+({user}[^\s]+)\s+""",
      """プライマリ ドメイン:\s+({domain}[^\s]+)\s+""",
      """プライマリ ログオン ID:\s+\([^,]+,\s*({login_id}[^)]+)""",
      """イメージ ファイル名:\s+({process_name}.+?)\s+プライマリ ユーザー名:""",
      """クライアント ユーザー名:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """アクセス数:\s+({access}.+?)\s+特権:"""
    ]
    ParserVersion = "v1.0.0"
  

}
```