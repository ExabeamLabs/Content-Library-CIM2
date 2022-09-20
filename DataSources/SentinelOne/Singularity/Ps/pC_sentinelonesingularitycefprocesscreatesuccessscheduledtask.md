#### Parser Content
```Java
{
Name = sentinelone-singularity-cef-process-create-success-scheduledtask
  Product = Singularity 
  Conditions = [ """CEF:""", """|Security|SentinelOne|""", """|scheduled_task|""" ]
  Fields = ${SentinelOneParsersTemplates.cef-sentinelone-security-alert.Fields}[
    """\staskName:(|({object}.+?))(\s+\w+:|\s*$)""",
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
      """\sagentIp:({dest_ip}[a-fA-F\d.:]+)""",
      """\sagentName:(|({dest_host}.+?))(\s+\w+:|\s*$)""",
      """\sagentfileFullNameGroupId:(|({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}\w+))?)))(\s+\w+:|\s*$)""",
      """\sprocessName:(|({process_name}.+?))(\s+\w+:|\s*$)""",
      """\sid:(|({alert_id}.+?))(\s+\w+:|\s*$)""",
    
}
```