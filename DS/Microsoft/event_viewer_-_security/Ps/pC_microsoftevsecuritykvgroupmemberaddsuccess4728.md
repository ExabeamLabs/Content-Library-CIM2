#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-add-success-4728
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """4728""", """セキュリティが有効なグローバル""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}[\w\-.]+),.+?グループにメンバーが追加されました。"""
  ]


}
```