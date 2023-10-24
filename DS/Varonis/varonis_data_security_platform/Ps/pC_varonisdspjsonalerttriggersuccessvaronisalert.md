#### Parser Content
```Java
{
Name = "varonis-dsp-json-alert-trigger-success-varonisalert"
 Vendor = "Varonis"
 Product = "Varonis Data Security Platform"
 TimeFormat = "MM/dd/yyyy hh:mm:ss a"
 Conditions = [
  """Varonis alert:"""
  """Alert details:"""
 ]
 Fields = [
   """Event Time:\s*({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
   """Device hostname:\s*(|({host}[\w\-.]+))\s+Additional Data:"""
   """Acting Object:\s*({domain}[^\\\s]+)\\"""
   """Acting Object SAM Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*File Server"""
   """IP Address/Host:\s*(({dest_ip}\d+\.\d+\.\d+\.\d+)|({dest_host}[^\s]+))"""
   """Device IP address:\s*(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s*Device"""
   """Rule Name:\s*({alert_name}.+?)(?:\s+Severity|\s*Rule Storyline):"""
   """Event Type:\s*({alert_type}.+?)\s*(?:IP Address|Event Status)"""
   """Severity:\s*({alert_severity}\d+)"""
   """Affected Object:\s*({file_name}.+?)\s*Event Type:"""
   """Path:\s*({additional_info}.+?)\s*Affected Object:"""
 ]
 ParserVersion = "v1.0.0"


}
```