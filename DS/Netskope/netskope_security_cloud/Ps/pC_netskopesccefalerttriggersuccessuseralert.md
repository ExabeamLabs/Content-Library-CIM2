#### Parser Content
```Java
{
Name = netskope-sc-cef-alert-trigger-success-useralert
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":"""", """"alert":"yes"""", """"action":"useralert"""" ]
  Fields = [
  """"timestamp":({time}\d{10})"""
  """"hostname":"({src_host}[\w\-\.]+)"""
  """"app":"({app}[^"]+)"""
  """"user":"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({domain}[^"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-]{1,40}\$?))))""""
  """"object":"(((?i)(Unknown( Unknown)?)|null)|({object}[^"]+?))\s*""""
  """"activity":"({operation}[^"]+)""""
  """"os":"((?i)unknown|({os}[^"]+))"""",
  """"browser":"((?i)unknown|({browser}[^"]+))"""",
  """"url":"({url}[^"]+)""""
  """"file_size":({bytes}\d+)""",
  """"file_type":"(Unknown|({file_type}[^"]+))"""",
  """"page_site":"({app}[^"]+)"""",
  """"action":"({action}[^"]+)"""
  """"alert_name":"({alert_name}[^"]+)""""
  """"alert_type":"({alert_type}[^"]+)""""
  """"severity":"({alert_severity}[^"]+)""""
  """"_id":"*({alert_id}[^",]+)"""
  """"userip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"src_location":"({src_location}[^"]+)"""
  """"src_country":"({src_country}[^"]+)"""
  ]
  DupFields = [ "object->file_name" ]
  ParserVersion = "v1.0.0"


}
```