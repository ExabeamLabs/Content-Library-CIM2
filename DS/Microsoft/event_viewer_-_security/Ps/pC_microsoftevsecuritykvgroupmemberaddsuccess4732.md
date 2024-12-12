#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-add-success-4732
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """4732""", """セキュリティが有効なローカル""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}[\w\-.]+),.+?グループにメンバーが追加されました。"""
  ]
  DupFields = [ "host->src_host" ]


}
```