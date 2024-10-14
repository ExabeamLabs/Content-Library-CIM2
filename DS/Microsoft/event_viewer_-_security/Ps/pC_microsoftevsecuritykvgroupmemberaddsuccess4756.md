#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-add-success-4756
  ParserVersion = v1.0.0
  Conditions = [ """4756""", """セキュリティが有効なユニバーサル""" ]

jp-member-added = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}[\w\-.]+),.+?グループにメンバーが追加さ
れました。""",
    """サブジェクト:.+?アカウント名:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """アカウント ドメイン:\s+({domain}[^\s]+)""",
    """ログオン ID:\s+({login_id}[^\s]+)\s+""",
    """メンバー:\s+セキュリティ ID:\s+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s:"]+))|({account_domain}[^\\]+)\\({account_name}.+?)|(?:.+?))\s+アカウント名:""",
    """メンバー:.+?アカウント名:\s*({user_dn}(?i)(cn)=.+?,({user_ou}OU.+?DC=[\w-]+))\s*グループ:""",
    """グループ:\s+セキュリティ ID:\s+({group_id}[^\s]+)""",
    """グループ:.+?アカウント名:\s+({group_name}.+?)?\s+アカウント ドメイン:""",
    """グループ:.+?グループ名:\s+({group_name}.+?)?\s+グループ ドメイン:""",
    """グループ:.+?グループ ドメイン:\s+({group_domain}[^\s]+)""",
    """セキュリティが有効な({group_type}[^\s]+)\s+グループにメンバーが追加されました。""",
  
}
```