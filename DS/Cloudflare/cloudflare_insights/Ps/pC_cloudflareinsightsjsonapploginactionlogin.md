#### Parser Content
```Java
{
Name = cloudflare-insights-json-app-login-actionlogin
  Vendor = Cloudflare
  Product = Cloudflare Insights
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =Cloudflare""", """"Action":"login"""", """"Allowed":""" ]
  Fields = [
    """exa_json_path=$.CreatedAt,exa_field_name=time"""
    """exa_json_path=$.Action,exa_field_name=operation"""
    """exa_json_path=$.IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.Email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.Connection,exa_field_name=auth_method"""
    """exa_json_path=$.Allowed,exa_field_name=result"""
    """exa_json_path=$.AppDomain,exa_field_name=domain"""
    """exa_json_path=$.UserUID,exa_field_name=user_uid"""
    """exa_json_path=$.Country,exa_field_name=country_code"""
    """exa_regex=destinationServiceName =({app}[^\s]+)"""
  ]


}
```