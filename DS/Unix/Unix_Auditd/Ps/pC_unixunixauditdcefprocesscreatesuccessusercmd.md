#### Parser Content
```Java
{
Name = unix-unixauditd-cef-process-create-success-usercmd
  Conditions = [ """CEF""", """Unix|auditd""", """USER_CMD""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """cmd\\=({command}[^\s]+)""",
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\"""
  ]
  ParserVersion = "v1.0.0"

cef-unix-template-1 = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\srt=({time}\d+)""",
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
      """src=({src_ip}[^\s]+)"""
      """dst=({dest_ip}[^\s]+)"""
      """spt=({src_port}\d+)""",
      """dpt=({dest_port}\d+)""",
      """\sduser=(\(unknown\)|({user}.+?))\s+\w+=""",
      """dhost=({dest_host}[^\s]+)""",
      """shost=({src_host}[^\s]+)"""
      
}
```