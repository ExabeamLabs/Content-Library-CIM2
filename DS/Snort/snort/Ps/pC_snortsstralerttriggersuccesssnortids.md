#### Parser Content
```Java
{
Name = snort-s-str-alert-trigger-success-snortids
  ParserVersion = v1.0.0
  Vendor = Snort
  Product = Snort
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ snort[""", """[SNORTIDS[""", """ || """ ]
  Fields = [
    """\s({host}[\w\-.]+)\s+snort\[""",
    """\[SNORTIDS\[[^"]*?({time}\d+-\d+-\d+\s+\d+:\d+:\d+)\S*\s+\d+\s+\[[^\]]*\]\s+({alert_name}[^\|]+?)\s*\|+\s*({alert_type}[^\|]*?)\s*\|+\s*({alert_severity}\d+)\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+[^\|]*?\|+[^\|]*?\|+\s*({additional_info}[^|]*?)\s*\|\|"""
  ]


}
```