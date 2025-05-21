#### Parser Content
```Java
{
Name = unix-ad-cef-endpoint-logout-success-userend
  ParserVersion = v1.0.0
  Conditions = [ """CEF""", """Unix|auditd""", """USER_END""" ]
  Fields = ${DLUnixParsersTemplates.cef-unix-template-1-dl.Fields}[
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\""",
    ]

cef-unix-template-1-dl = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\srt=({time}\d{13})""",
      """\sdvc(host)?=({host}[^\s]+)"""
      """\sduid=({user_id}\d+)""",
      """\ssuid=({user_id}\d+)""",
      """auid=({account_id}\d+)""",
      """cat=({operation}[^\|\s]+)""",
      """destinationServiceName =({service_name}[^\s]+)""",
      """\WeventId=({event_id}\d+)"""
      """\Wcs4=({process_id}\d+)""",
      """\sdproc=({process_path}({process_dir}[^\s]*?[\\\/]+)?({process_name}[^\s\\\/]+))\s+\w+=""",
      """categoryOutcome=\/({result}[^\s]+)""",
      """\Wagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """spt=({src_port}\d+)""",
      """dpt=({dest_port}\d+)""",
      """\sduser=(\(unknown\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
      """dhost=({dest_host}[^\s]+)""",
      """shost=({src_host}[^\s]+)"""
      
}
```