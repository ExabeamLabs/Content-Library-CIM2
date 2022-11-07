#### Parser Content
```Java
{
Name = accellion-kw-json-app-activity-success-networksettings
  Product = Kiteworks
  Conditions = [ """url_host""", """app_host""", """description""", """network_settings""", """event""" ]
  Fields = ${KiteWorksParsersTemplates.accelion-kite-app.Fields}[
    """"+proxy_ip\"+.+to\s+\"+({proxy_ip}[^\/]+)""",
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
    """"+user_ip"+:\s*"+({src_ip}[^"]+)"+""",
    """"+application"+:\s*"+({app}[^"]+)"+""",
    """"+app_host"+:\s*"+({host}[^"]+)"+""",
    """"+event"+:\s*"+({access}[^"]+)"+""",
    """"+user_agent"+:\s+"+({user_agent}[^"]+)?"+\,""",
    """"+url_host"+:\s*"+({url_host}[^"]+)?"+\,""",
    """"+size"+:\s*({bytes}\d+)""",
    """"+mime":\s*"({mime}[^"]+)""",
  
}
```