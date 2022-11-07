#### Parser Content
```Java
{
Name = ibm-racf-kv-app-activity-general-audit-record-auditrecordwritten
Vendor = IBM
Product = IBM Racf
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS""", """EVNTNAME=AUDIT""", """EVNTTEXT=General audit record written"""]
Fields = [
  """APPLSIEMVRM=({host}[^=]+?)\s\w+=""",
  """APPLHOSTIPADD=({host_ip}[A-Fa-f.:\d]+)""",
  """EVNTUSERID=({db_user}[^=]+?)\s\w+=""",
  """EVNTNAME=({event_name}[^=]+?)\s\w+=""",
  """EVNTJOBNAME=({service_name}[^=]+?)\s\w+=""",
  """EVNTUSERNAME=(\-*N\/A\-*|({user}[^=]+?))\s\w+=""",
  """EVNTTEXT=({additional_info}[^=]+?)\s\w+=""",
  """EVNTCOMMAND=(\-*N\/A\-*|({db_query}[^=]+?))(\s\w+=|\s*$)""",
  """EVNTCLASSNAME=({db_object}[^=]+?)\s*\w+="""
  ]
 

}
```