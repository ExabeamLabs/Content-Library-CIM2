#### Parser Content
```Java
{
Name = "symantec-wss-str-endpoint-notification-success-lookupfailedforgroup"
  ParserVersion = "v1.0.0"
  Conditions = [ """ ProxySG: """, """ Group cache: Lookup failed for group """ ]
  Fields = ${SymantecParsersTemplates.symantec-wss-template.Fields}[
    """ ProxySG: ({event_code}[^\s]+)\s+({event_name}[^"]+)\s+({severity}\w+_(ERROR|EVENT))"""
    """for group (({group_domain}[^\\]+)[\\]+({group_name}[^\s]+?))\.\s"""
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