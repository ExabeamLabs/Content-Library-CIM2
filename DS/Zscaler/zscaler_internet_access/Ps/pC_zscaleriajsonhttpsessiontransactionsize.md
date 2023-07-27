#### Parser Content
```Java
{
Name = zscaler-ia-json-http-session-transactionsize
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"transactionsize":"""", """"threatcategory":"""", """"dlpengine":"""", """"url":"""", """"vendor":"Zscaler"""", """"product":"NSS"""", """"protocol":""", """"useragent":""" ]
  Fields = [
    """"datetime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"protocol":"({protocol}[^"]+)"""",
    """"action":"({action}[^"]+)"""",
    """"responsesize":"({bytes_in}\d+)"""",
    """"requestsize":"({bytes_out}\d+)"""",
    """"transactionsize":"({bytes}\d+)"""",
    """"urlsupercategory":"({category}[^"]+)""""
    """"urlcategory":"({category}[^"]+)"""",
    """"serverip":"({dest_ip}[a-fA-F\d:\.]+)"""",
    """"requestmethod":"(NA|({method}[^"]+))"""",
    """"refererURL":"(None|({referrer}[^"]+))"""",
    """"useragent":"(Unknown|({user_agent}[^"]+))"""",
    """"clientip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"status":"({result_code}\d{1,3})"""",
    """"user":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|(AWS|([^"]+?->[^"]+)|({user}[\w\.\-]{1,40}\$?)))"""",
    """"url":"({url}(\w{1,5}:\/\/)?[^"\/\?]+({uri_path}\/[^"\?]*)?(\?({uri_query}[^"]*))?)"""",
    """"hostname":"({web_domain}[^"]+)"""",
    """"appname":"({app}[^"]+)"""",
    """"reason":"(Allowed|({failure_reason}[^"]+))"""",
    """"devicehostname":"(NA|({src_host}[\w\.\-]+))""""
  ]


}
```