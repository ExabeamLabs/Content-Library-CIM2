#### Parser Content
```Java
{
Name = netskope-sc-json-app-login-success-loginsuccessful
  Conditions = [ """"appcategory": """, """"type": """, """"activity": "Login Successful"""" ]
  ParserVersion = "v1.0.0"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.hostname,exa_field_name=src_host"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.srcip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.user,exa_regex=(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-]{1,40}\$?))))"""
    """exa_json_path=$.access_method,exa_field_name=time"""
    """exa_json_path=$.logintype,exa_field_name=auth_method"""
    """exa_json_path=$.activity,exa_field_name=operation"""
    """exa_json_path=$.os,exa_field_name=os"""
    """exa_json_path=$.browser,exa_field_name=browser"""
    """exa_json_path=$.page,exa_field_name=web_domain"""
    """exa_json_path=$.url,exa_field_name=url"""
    """exa_json_path=$.dst_location,exa_field_name=location"""
    """exa_json_path=$.page_site,exa_field_name=app"""
    """exa_json_path=$.referer,exa_field_name=referrer"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]


}
```