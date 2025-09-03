#### Parser Content
```Java
{
Name = akamai-guardicore-cef-network-traffic-blocked-networklog
    Vendor = Akamai 
    Product = Akamai Guardicore
    TimeFormat = "epoch_sec"
    Conditions = [ """CEF:""" , """Guardicore|Centra""", """|Network Log|""", """act=Blocked""" ]
    Fields = [
      """start=({time}\d{10})""",
      """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""", 
      """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)""", 
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """shost=({src_host}[\w\-\.]+)""",
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """dhost=({dest_host}[\w\-\.]+)""",
      """suser=(((?i)NT AUTHORITY|({src_domain}[^\\]+))[\\]+)?((?i)SYSTEM|LOCAL SERVICE|NETWORK SERVICE|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """duser=(((?i)NT AUTHORITY|({dest_domain}[^\\]+))[\\]+)?((?i)SYSTEM|LOCAL SERVICE|NETWORK SERVICE|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """proto=({protocol}[^=]+)\s+\w+="""
      """dpt=({dest_port}\d+)""",
      """act=({action}[^=]+)\s+\w+=""",
      """cs1=({connection_type}[^\s]+)\s+\w+=""",
      """cs2=({additional_info}[^=]+)\s+\w+=""",
      """cs4=({more_info}[^=]+)\s+\w+="""
      """cs13=({src_process_path}({src_process_dir}(?:\w+:|\/)*(?:[\\\/]+[\w\s\.\-\(\)]+)*[\\\/]+)({src_process_name}[\w\-.]+)*)""",
      """cs14=({app}[^=]+)(?:\s\w+|$)""",
      """cs15=({dest_process_path}({dest_process_dir}(?:\w+:|\/)*(?:[\\\/]+[\w\s\.\-\(\)]+)*[\\\/]+)({dest_process_name}[\w\-.]+)*)""",
      """cs16=({app}[^=]+)(?:\s\w+|$)""",
      ]
    ParserVersion = v1.0.0


}
```