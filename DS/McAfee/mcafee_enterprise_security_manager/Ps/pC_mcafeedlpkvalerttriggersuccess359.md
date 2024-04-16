#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-359
    Vendor = McAfee
    Product = McAfee Enterprise Security Manager
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """|McAfee|ESM|""", """|359-""", """act=alert""" ]
    Fields = [
      """\send=({time}\d{13})""",
      """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sshost=({src_host}[^\s]+)""",
      """\|McAfee\|ESM\|[^\|]+\|359-({signature_id}[^\|]+)""",
      """\seventId=({alert_id}[^\s]+)\s[^\s]+?=""",
      """\snitroThreat_Name =({alert_name}.+?)\s[^\s]+?=""",
      """\snitroObject_Type=({alert_type}.+?)\s[^\s]+?=""",
      """\sduser=([^\\=]+?\\)?({user}[\w\.\-]{1,40}\$?)\s[^\s]+?=""",
      """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\snitroProcess_Name =({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\s[^\s]+="""
    ]
    ParserVersion = "v1.0.0"
  

}
```