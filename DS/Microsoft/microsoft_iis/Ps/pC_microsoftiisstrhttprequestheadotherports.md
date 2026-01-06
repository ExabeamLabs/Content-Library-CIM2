#### Parser Content
```Java
{
Name = microsoft-iis-str-http-request-headotherports
  Vendor = "Microsoft"
  Product = "Microsoft IIS"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy:HH:mm:ss zzz"]
  Conditions = [ """HEAD /""" ]
  VendorMatch = true
  Fields = [
    """({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+({method}[A-Z]+)\s+(-|({uri_path}\/[^\s]*))\s+(-|({uri_query}[^\s]*))\s+({=src_port}\d+)\s+(-|({user}[\w\.\-]{1,40}\$?))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(-|({referrer}[^\s]*))\s+(-|({user_agent}[^\s]*))\s+({http_response_code}\d{3})\s+({sub_status}\d{1,3})\s+({error_code}\d{1,3})\s+({bytes_in}\d+)"""
    """({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})"""
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+HEAD\s+(-|({uri_path}\/[^\s]*))\s+(-|({uri_query}[^\s]*))\s+({src_port}\d+)\s+(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\]+)\\)?({user}[\w\.\-]{1,40}\$?))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+(-|({referrer}[^\s]*))\s+(\d+)?\s*(-|({user_agent}[^\s]*))\s+((-|[^\s]+\s+){2}\s+)?(-|({web_domain}[^\s:]+))(:[^\s]+)?\s+({http_response_code}\d{3})\s+({sub_status}\d{1,3})\s+({error_code}\d{1,3})\s+({bytes_in}\d+)\s+({bytes_out}\d+)\s+"""
  ]
  ParserVersion = "v1.0.0"


}
```