#### Parser Content
```Java
{
Name = vbcorp-v-kv-alert-trigger-success-vbcorp
  ParserVersion = v1.0.0
  Vendor = VBCorp
  Product = VBCorp
  TimeFormat = "yyyy/MM/dd HH:mm:ss Z"
  Conditions = ["""Product=VBCorp""" , """グレーウェア"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """日時:\s*({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d (\+|\-)\d\d:\d\d)""",
    """\shost=({host}[^\s]+)""",
    """(?:ユーザ名|ユーザ吁):?\s*(|({user}.+?))\s*IP""",
    """IPアドレス:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*""",
    """MAC アドレス:\s*({src_mac}[^\s]+)\s*""",
    """({alert_type}(?:ウイルス\/不正プログラム|スパイウェア\/グレーウェア)):\s*({alert_name}[^\s]+)\s*""",
    """エンドポイント:\s*({src_host}[^\s]+)\s*""",
    """ドメイン:\s*({domain}.+?)\\?\s*(ファイル:|日時:)""",
    """ファイル:\s*(|({malware_url}.+?))\s+(日時:|\w+)\s*\d\d\d\d\/\d\d\/\d\d""",
    """結果:\s*(|({result}[^"]+?))\s*""",
  ]


}
```