#### Parser Content
```Java
{
Name = ibm-racf-kv-app-activity-general-audit-record-auditrecordwritten
Vendor = IBM
Product = IBM Resource Access Control Facility
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS""", """EVNTNAME=AUDIT""", """EVNTTEXT=General audit record written"""]
Fields = [
  """APPLSIEMVRM=({host}[^=]+?)\s\w+=""",
  """APPLHOSTIPADD=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
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