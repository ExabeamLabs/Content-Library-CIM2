#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-success-browsersession
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [""""app":""", """"access_method":""", """"category":""", """"browser_session_id":""", """"src-application-name":"Netskope""""]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.event-name,exa_field_name=event_name"""
    """exa_json_path=$.src-ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.user,exa_regex=(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.domain,exa_field_name=domain"""
    """exa_json_path=$.user-email,exa_regex=(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.useragent,exa_field_name=user_agent"""
    """exa_json_path=$.type,exa_field_name=operation"""
  ]
  ParserVersion = "v1.0.0"


}
```