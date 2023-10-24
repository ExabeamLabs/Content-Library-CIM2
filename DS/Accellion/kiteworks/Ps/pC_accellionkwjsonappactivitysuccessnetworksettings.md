#### Parser Content
```Java
{
Name = accellion-kw-json-app-activity-success-networksettings
  Product = Kiteworks
  Conditions = [ """url_host""", """app_host""", """description""", """network_settings""", """event""" ]
  Fields = ${KiteWorksParsersTemplates.accelion-kite-app.Fields}[
    """proxy_ip\\"+.+to\s+\\"+({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """"+description"+:\s+"+({additional_info}.*?)""*\,\s"+successful"""
    ]
   DupFields = [ "additional_info->operation" ]
   ParserVersion = "v1.0.0"

accelion-kite-app = {
  Vendor = Accellion
  Product = Kiteworks
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"+description"+:\s+"+\/*:*({additional_info}[^,]+)"""",
    """"+user_name"+:\s*"+(System|({email_address}[^@]+@({email_domain}[^"]+)))"+"""
    """"+user_ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+""",
    """"+application"+:\s*"+({app}[^"]+)"+""",
    """"+app_host"+:\s*"+({host}[^"]+)"+""",
    """"+event"+:\s*"+({access}[^"]+)"+""",
    """"+user_agent"+:\s+"+({user_agent}[^"]+)?"+\,""",
    """"+url_host"+:\s*"+({url_host}[^"]+)?"+\,""",
    """"+size"+:\s*({bytes}\d+)""",
    """"+mime":\s*"({mime}[^"]+)""",
  
}
```