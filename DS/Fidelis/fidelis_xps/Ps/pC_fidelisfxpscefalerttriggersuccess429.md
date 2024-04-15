#### Parser Content
```Java
{
Name = "fidelis-fxps-cef-alert-trigger-success-429"
Vendor = "Fidelis"
Product = "Fidelis XPS"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM|"""
"""|429-"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|[^|]*\s({alert_type}[^\s]+)\s({alert_name}(FSS_|Malware|DNS)[^|]+?)\|"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|"""
"""\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sexternalId=({alert_id}\d+)"""
"""\sshost=({src_host}[^\s|]+)"""
"""\sspt=({src_port}\d+)"""
"""\sdpt=({dest_port}\d+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\ssntdom=(?:<n\/a>|({malware_url}.+?))\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```