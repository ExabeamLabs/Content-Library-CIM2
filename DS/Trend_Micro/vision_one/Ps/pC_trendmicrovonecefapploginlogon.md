#### Parser Content
```Java
{
Name = "trendmicro-vone-cef-app-login-logon"
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Trend Micro|Trend Vision One|""", """|900003|""", """ cs3=Log on""" ]
   Fields = ${TrendMicroParserTemplates.trendmicro-vision-one-account-audit.Fields}[
     """'Endpoint IP address':\s*'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'""",
     """'Appliance name':\s*'({src_host}[\w.-]+)'""",
     """'Device ID':\s*'({device_id}[^']+)'"""
   ]
 
trendmicro-vision-one-account-audit = { 
  Vendor = Trend Micro
  Product = Vision One
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """CEF:([^\|]*\|){4}({event_code}[^|]+)""",
    """CEF:([^\|]*\|){5}({event_category}[^|]+)""",    
    """cat=((?i)Unknown|({category}[^=,]+))(\s*,\S+)?\s+\w+=""",
    """({app}Trend Vision One)""",
    """ \d\d:\d\d:\d\d ({host}[\w.-]+)\s""",
    """ cn1=({result}\d)""", 
    """ cs1=(({user}[\w\.\-\!\#\^\~]{1,40})|({full_name}[^=]+?))((\s+\w+=)|\s*$)""",
    """ cs2=({role}[^=]+?)((\s+\w+=)|\s*$)""",
    """ cs3=({event_name}[^=]+?)((\s+\w+=)|\s*$)""",
    """ msg=\{({additional_info}[^=]+?)\}\s*(\s*$|(\s+\w+=))"""
  ]
  DupFields = [ "event_name->operation" 
}
```