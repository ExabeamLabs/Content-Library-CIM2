#### Parser Content
```Java
{
Name = airlock-waf-kv-file-write-success-createfolder
  Product = Web Application Firewall
  Conditions = [ """ Audit Log [""", """ event_type="""", """" time_taken="""", """" system_name="""", """"Create Folder Successful"""" ]
  Fields = ${AirlockTemplates.AirlockEvent.Fields}[
      """\sfile_path="(\w+:_)?({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+))""",
  ]
  ParserVersion = v1.0.0

AirlockEvent = {
    Vendor = Airlock
    TimeFormat = "M/d/yy h:mm:ss a"
    Fields = [
      """\sstart_time="({time}\d+\/\d+\/\d+ \d+:\d+:\d+ \w+)""",
      """\sseverity="({alert_severity}[^"]+)"""",
      """\ssystem_name="({host}[^"]+)"""",
      """\ssession_id="({session_id}[^"]+)"""",
      """\sremote_port="({src_port}\d+)"""",
      """\sremote_ip="({src_ip}[^"]+)"""",
      """\sremarks="({operation}[^"]+)"""",
      """\slocal_port="({dest_port}\d+)"""",
      """\slocal_ip="({dest_ip}[^"]+)"""",
      """\sevent_type="({event_name}[^"]+)"""",
      """\sevent_id="({event_code}[^"]+)"""",
      """\scommand="({action}[^"]+)"""",
      """\suser_name="(unknown|({user}[^"]+))"""",
      """\sdomain="(Default|({domain}[^"]+))"""",
      """\sfile_size="({bytes}\d+)"""",
      """\sfile_path="(\w+:_)?({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+?(\.({file_ext}[^\\\/\.;"]+))))"""
      """\sfile_path="(\w+:_)?({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+(\.({file_ext}[^\\\/\.;"]+))))"""
    ]
    DupFields = ["host->dest_host"
}
```