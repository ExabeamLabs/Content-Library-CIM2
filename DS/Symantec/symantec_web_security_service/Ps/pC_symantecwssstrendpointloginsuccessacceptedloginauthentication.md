#### Parser Content
```Java
{
Name = "symantec-wss-str-endpoint-login-success-acceptedloginauthentication"
  ParserVersion = "v1.0.0"
  Conditions = [ """ ProxySG: """, """ SSH: Accepted, login-authentication""" ]
  Fields = ${SymantecParsersTemplates.symantec-wss-template.Fields}[
    """ ProxySG: ({event_code}[^\s]+)\s({event_category}SSH)[^:]*:\s*({event_name}Accepted, login-authentication)"""
    """user "({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """port "({src_port}\d+)"""
    """protocol "({protocol}[^"]+)"""
    """realm "({realm}[^"]+)"""
    """({severity}\w+_(ERROR|EVENT))"""
  ]
  ParserVersion = "v1.0.0"

symantec-wss-template = {
    Vendor = "Symantec"
    Product = "Symantec Web Security Service"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
      """:\d\d:\d\d ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? """
      """({host}[\w.-]+) ProxySG:"""
    ]
    DupFields = [ "host->dest_host" 
}
```