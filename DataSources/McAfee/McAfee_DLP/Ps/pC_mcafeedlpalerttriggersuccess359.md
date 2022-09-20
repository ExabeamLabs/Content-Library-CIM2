#### Parser Content
```Java
{
Name = mcafee-dlp-alert-trigger-success-359
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|ESM|""", """|359-""", """act=alert""" ]
    Fields = [
      """\send=({time}\d+)""",
      """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\sshost=({src_host}[^\s]+)""",
      """\|McAfee\|ESM\|[^\|]+\|359-({signature_id}[^\|]+)""",
      """\seventId=({alert_id}[^\s]+)\s[^\s]+?=""",
      """\snitroThreat_Name =({alert_name}.+?)\s[^\s]+?=""",
      """\snitroObject_Type=({alert_type}.+?)\s[^\s]+?=""",
      """\sduser=([^\\=]+?\\)?({user}.+?)\s[^\s]+?=""",
      """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\snitroProcess_Name =({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\s[^\s]+="""
    ]
    ParserVersion = "v1.0.0"
  

}
```