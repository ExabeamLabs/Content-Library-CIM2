#### Parser Content
```Java
{
Name = "liquidfiles-l-json-app-notification-success-csrferror"
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [ """liquidfiles[""", """"message":"CSRF error for User:""" ]
  Fields = ${LiquidFilesParserTemplates.Liquid-json-template.Fields}[
    """CSRF error for User:.+?from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  ]

Liquid-json-template = {
    Vendor = "LiquidFiles"
    Product = "LiquidFiles"
    TimeFormat = "MMM dd HH:mm:ss"
    Fields = [
      """({time}\w\w\w \d\d \d\d:\d\d:\d\d)"""
      """({app}liquidfiles)""",
      """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"message":"({event_name}[^:"]+)""",
      """"username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?))"""",
      """"hostname":"({host}[^"]+)"""
      """"access_method":({method}[^"]+)""""
      """"user_email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """"log_level":"({run_level}[^"]+?)\s*""""
      """"error":"({failure_reason}[^"]+)""""
      """"filename":"({file_name}[^"]+)""""
      ]
    }
  }
#============================================== Start of DefaultParsersAA section ==================================================================
DefaultParsersAA = [

{
Name = "appsense-am-leef-alert-trigger-success-warning"
Vendor = "AppSense"
Product = "AppSense Application Manager"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a"]
Conditions = [
"""AppSense Application Manager"""
"""SourceName ="""
"""Message="""
"""EventCode="""
]
Fields = [
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""ComputerName =({dest_host}[^\s]+)"""
"""Sid=({dest_user_sid}[^\s]+)"""
"""\s+Type=({alert_severity}[^\s]+)"""
"""\'\w+:\\+(?i)users\\+({user}[\w\.\-]{1,40}\$?)"""
"""Hash:({hash_md5}[^\s\]]+)"""
"""Vendor:\s+({process_vendor}[^\]]+)"""
"""Message=AppSense Application Manager ({alert_name}.+?)\s+(of [^\w]|\'|for)"""
"""Message=(The file )?\'.+?\'( has had)?\s+({alert_name}.+?)\s*(\.|of|for)"""
"""Message=\'(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\'"""
"""\'({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?))(\s+\[\w+:|')"""
]
DupFields = [
"process_path->path"
"dest_host->host"
"alert_name->alert_type"
"user_sid->account_id"
]
ParserVersion = "v1.0.0"
}


{
  Name = openvpn-ov-json-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ 
""" openvpn[""" 
"""MULTI_sva: pool returned """
"""IPv4=""" 
]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """ openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """hostname":"({host}[^"]+)""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_regex= openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """exa_regex=IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """exa_json_path=$.beat.hostname,exa_field_name=host"""
  ]
  DupFields = [ "user->account" 
}
```