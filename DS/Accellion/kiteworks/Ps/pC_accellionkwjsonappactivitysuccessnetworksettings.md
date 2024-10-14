#### Parser Content
```Java
{
Name = accellion-kw-json-app-activity-success-networksettings
  ExtractionType = json
  Product = Kiteworks
  Conditions = [ """url_host""", """app_host""", """description""", """network_settings""", """event""" ]
  Fields = ${KiteWorksParsersTemplates.accelion-kite-app.Fields}[
    """proxy_ip\\"+.+to\s+\\"+({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """"+description"+:\s+"+({additional_info}.*?)""*\,\s"+successful"""
    """exa_regex=proxy_ip\\"+.+to\s+\\"+({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$.description,exa_field_name=additional_info""",
    ]
   DupFields = [ "additional_info->operation" ]
   ParserVersion = "v1.0.0"

accelion-kite-app = {
  Vendor = Accellion
  Product = Kiteworks
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"+description"+:\s+"+\/*:*({additional_info}[^,]+)"""",
    """"+user_name"+:\s*"+(System|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"+"""
    """"+user_ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+""",
    """"+application"+:\s*"+({app}[^"]+)"+""",
    """"+app_host"+:\s*"+({host}[^"]+)"+""",
    """"+event"+:\s*"+({access}[^"]+)"+""",
    """"+user_agent"+:\s+"+({user_agent}[^"]+)?"+\,""",
    """"+url_host"+:\s*"+({web_domain}[^"]+)?"+\,""",
    """"+size"+:\s*({bytes}\d+)""",
    """"+mime":\s*"({mime}[^"]+)""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_regex="+user_name"+:\s*"+(System|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"+"""
    """exa_regex="+user_ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+""",
    """exa_json_path=$.application,exa_field_name=app""",
    """exa_json_path=$.app_host,exa_field_name=host""",
    """exa_json_path=$.event,exa_field_name=access""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent""",
    """exa_json_path=$.url_host,exa_field_name=web_domain""",
    """exa_json_path=$.size,exa_field_name=bytes""",
    """exa_json_path=$.mime,exa_field_name=mime""",
  
}
```