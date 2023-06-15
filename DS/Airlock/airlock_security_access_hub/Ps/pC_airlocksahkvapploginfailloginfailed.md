#### Parser Content
```Java
{
Name = airlock-sah-kv-app-login-fail-loginfailed
  Product = Airlock Security Access Hub
  Conditions = [ """ Audit Log [""", """ event_type="""", """" time_taken="""", """" system_name="""", """"Login Failed"""" ]
  Fields = ${AirlockTemplates.AirlockEvent.Fields}[
    """\sremarks="({failure_reason}[^"]+)"""", 
  ]
  ParserVersion = "v1.0.0"

AirlockEvent = {
    Vendor = Airlock
    TimeFormat = "M/d/yy h:mm:ss a"
    Fields = [
      """\sstart_time="({time}\d+\/\d+\/\d+ \d+:\d+:\d+ \w+)""",
      """\sseverity="({alert_severity}[^"]+)"""",
      """\ssystem_name="({host}[^"]+)"""",
      """\ssession_id="({session_id}[^"]+)"""",
      """\sremote_port="({src_port}\d+)"""",
      """\sremote_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """\sremarks="({operation}[^"]+)"""",
      """\slocal_port="({dest_port}\d+)"""",
      """\slocal_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
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