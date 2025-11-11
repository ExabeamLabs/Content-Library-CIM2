#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-group-member-add-success-memberadded
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MM/dd/yyyy hh:mm:ss a"
    Conditions = [ """EventCode=""", """セキュリティが有効な""" ]
    Fields = [ 
      """ComputerName =({computer_name}({host}[\w.\-]+))""",
      """EventCode=({event_code}[\w]+)""",
      """セキュリティが有効な({group_type}[^\s]+) グループにメンバーが追加されました。""",
      """サブジェクト:.+?アカウント名:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """アカウント ドメイン:\s+({domain}[^\s]+)""",
      """ログオン ID:\s+({login_id}[^\s]+)\s+""",
      """メンバー:\s+セキュリティ ID:\s+(({dest_user_sid}S-\d+-[^:\s]+)|({account_domain}[^\\]+)\\+({account_name}.+?)|(?:.+?))\s+アカウント名:""",
      """メンバー:.+?アカウント名:\s*({user_dn}.+?)\s*グループ:""",
      """グループ:\s+セキュリティ ID:\s+({group_id}[^\s]+)""",
      """グループ:.+?グループ名:\s+({group_name}.+?)?\s+グループ ドメイン:""",
      """グループ:.+?グループ ドメイン:\s+({group_domain}[^\s]+)"""]
  

}
```