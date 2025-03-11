#### Parser Content
```Java
{
Name = netskope-sc-cef-alert-trigger-success-useralert
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":""", """"alert":""", """"action":""", """"yes"""", """"useralert"""" ]
  Fields = [
  """"timestamp":\s*({time}\d{10})"""
  """"hostname":\s*"({src_host}[\w\-\.]+)"""
  """"app":\s*"({app}[^"]+)"""
  """"user":\s*"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({domain}[^"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))""""
  """"object":\s*"(((?i)(Unknown( Unknown)?)|null)|({object}[^"]+?))\s*""""
  """"activity":\s*"({operation}[^"]+)""""
  """"os":\s*"((?i)unknown|({os}[^"]+))"""",
  """"browser":\s*"((?i)unknown|({browser}[^"]+))"""",
  """"url":\s*"({url}[^"]+)""""
  """"file_size":\s*({bytes}\d+)""",
  """"file_type":\s*"(Unknown|({file_type}[^"]+))"""",
  """"page_site":\s*"({app}[^"]+)"""",
  """"action":\s*"({action}[^"]+)"""
  """"alert_name":\s*"({alert_name}[^"]+)""""
  """"alert_type":\s*"({alert_type}[^"]+)""""
  """"severity":\s*"({alert_severity}[^"]+)""""
  """"_id":\s*"*({alert_id}[^",]+)"""
  """"userip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"src_location":\s*"({src_location}[^"]+)"""
  """"src_country":\s*"({src_country}[^"]+)"""
  """"dlp_rule_severity":"({alert_severity}[^"]+)""""
  """"dlp_rule_count":({rule_count}\d+)"""
  """"dlp_rule":"({rule}[^"]+)"""
  ]
  DupFields = [ "object->file_name" ]
  ParserVersion = "v1.0.0"


}
```