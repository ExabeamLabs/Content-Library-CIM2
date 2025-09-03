#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-add-success-4756
  ParserVersion = v1.0.0
  Conditions = [ """4756""", """セキュリティが有効なユニバーサル""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}[\w\-.]+),.+?グループにメンバーが追加されました。"""
  ]


}
```