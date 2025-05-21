#### Parser Content
```Java
{
Name = akamai-guardicore-cef-alert-trigger-success-networklog-1
    Vendor = Akamai 
    Product = Akamai Guardicore
    TimeFormat = "yyyy-MM-dd'T'HH:mmZ"
    Conditions = [ """CEF:""" , """Guardicore|Centra""", """|Network Log|""", """act=Alerted""" ]
    Fields = [
      """start=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\dZ)""",
      """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""", 
      """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)""", 
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """duser=(((?i)NT AUTHORITY|({dest_domain}[^\\]+))[\\]+)?((?i)SYSTEM|LOCAL SERVICE|NETWORK SERVICE|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """proto=({protocol}[^=]+)\s\w+="""
      """dpt=({dest_port}\d+)""",
      """act=({action}[^=]+)\s+\w+=""",
      """dhost=({web_domain}[^\s]+)\s+\w+="""
    ]
    ParserVersion = v1.0.0
  

}
```