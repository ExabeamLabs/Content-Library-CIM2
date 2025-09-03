#### Parser Content
```Java
{
Name = skyhighsecurity-ssc-csv-http-session-fail-denied
  Vendor = Skyhigh Security
  Product = Skyhigh Security Cloud
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Logging-Client """, """DENIED""" ]
  Fields = [
  """({action}DENIED)"""
  """Logging-Client\s"[^"]+","({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}[^"]+)""""
  """Logging-Client\s"(([^"]+)","){6}({url}[^"]+)""""
  """Logging-Client.*?DENIED","*,"(([^"]+"),")({time}\d{4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})","({protocol}[^"]+)","({categories}[^"]+)","({mime}[^"]+)","(|([^"]+))","(([^"]+"),")({failure_reason}[^"]+)","({result_code}[^"]+)","({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","*,"(([^"]+)","){4}({app}[^"]+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({dest_port}\d{1,5})","({country_code}[^"]+)","((|([^"]+))","){6}({src_host}[\w\-\.]+)""""
  """(?i)({log_source}Logging-Client)"""
  ]
  ParserVersion = "v1.0.0"
 

}
```