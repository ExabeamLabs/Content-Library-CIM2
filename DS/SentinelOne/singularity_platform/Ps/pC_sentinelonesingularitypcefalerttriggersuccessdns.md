#### Parser Content
```Java
{
Name = sentinelone-singularityp-cef-alert-trigger-success-dns
  Product = Singularity Platform
  Conditions = [ """CEF:""", """|Security|SentinelOne|""", """|dns|""" ]
  Fields = ${SentinelOneParsersTemplates.cef-sentinelone-security-alert.Fields}[
    """\sdnsRequest:({query}[^\s]+)""",
    """\sdnsResponse:(|({response}.+?))(\s+\w+:|\s*$)""",
  ]
  ParserVersion = "v1.0.0"

cef-sentinelone-security-alert = {
  Vendor = SentinelOne
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s+({host}\S+)""",
    """\seventType:(|({alert_type}.+?))(\s+\w+:|\s*$)""",
    """\sagentId:(|({agent_id}.+?))(\s+\w+:|\s*$)""",
    """\sagentIp:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sagentName:(|({dest_host}.+?))(\s+\w+:|\s*$)""",
    """\sagentfileFullNameGroupId:(|({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}\w+))?)))(\s+\w+:|\s*$)""",
    """\sprocessName:(|({process_name}.+?))(\s+\w+:|\s*$)""",
    """\sid:(|({alert_id}.+?))(\s+\w+:|\s*$)""",
  
}
```