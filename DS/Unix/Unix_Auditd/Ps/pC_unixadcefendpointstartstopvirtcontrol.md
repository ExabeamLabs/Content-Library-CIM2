#### Parser Content
```Java
{
Name = unix-ad-cef-endpoint-start-stop-virtcontrol
  ParserVersion = v1.0.0
  Conditions = [ """CEF""", """Unix|auditd""", """VIRT_CONTROL """ ]
  Fields = ${DLUnixParsersTemplates.cef-unix-template-1-dl.Fields}[
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\""",
    """act=({operation}[^\s]+)"""
    ]

cef-unix-template-1-dl = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\srt=({time}\d+)""",
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
      """\Wagt=({src_ip}[A-Fa-f:\d.]+)""",
      """src=({src_ip}[^\s]+)"""
      """dst=({dest_ip}[^\s]+)"""
      """spt=({src_port}\d+)""",
      """dpt=({dest_port}\d+)""",
      """\sduser=(\(unknown\)|({user}.+?))\s+\w+=""",
      """dhost=({dest_host}[^\s]+)""",
      """shost=({src_host}[^\s]+)"""
      
}
```