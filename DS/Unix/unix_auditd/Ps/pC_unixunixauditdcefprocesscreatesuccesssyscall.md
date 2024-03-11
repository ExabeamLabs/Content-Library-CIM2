#### Parser Content
```Java
{
Name = unix-unixauditd-cef-process-create-success-syscall
  Conditions = [ """CEF""", """Unix|auditd""", """SYSCALL""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """CEF:([^\|]*\|){5}({event_name}[^\\\|]+)\|({result}[^\|]+)"""
  ]
  ParserVersion = "v1.0.0"

cef-unix-template-1 = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\srt=({time}\d{13})""",
      """\Wagt=({host}[A-Fa-f:\d.]+)""",
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
      """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """spt=({src_port}\d+)""",
      """dpt=({dest_port}\d+)""",
      """\sduser=(\(unknown\)|({user}.+?))\s+\w+=""",
      """dhost=({dest_host}[^\s]+)""",
      """shost=({src_host}[^\s]+)"""
      
}
```