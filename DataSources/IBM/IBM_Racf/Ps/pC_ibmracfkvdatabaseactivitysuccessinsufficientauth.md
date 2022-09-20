#### Parser Content
```Java
{
Name = ibm-racf-kv-database-activity-success-insufficientauth
  ParserVersion = v1.0.0
  Product = IBM Racf
  Conditions = [ """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS""", """EVNTNAME=Access""", """EVNTTEXT=Insufficient authority""" ]

ibm-racf-activity = {
Vendor = IBM
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """APPLSIEMVRM=({host}[^=]+?)\s\w+=""",
  """APPLHOSTIPADD=({host_ip}[A-Fa-f.:\d]+)""",
  """EVNTUSERID=({db_user}[^=]+?)\s\w+=""",
  """EVNTNAME=({event_name}[^=]+?)\s\w+=""",
  """EVNTUSERNAME=(\-*N\/A\-*|({user}[^=]+?))\s\w+=""",
  """EVNTTEXT=({additional_info}[^=]+?)\s\w+=""",
  """EVNTCOMMAND=(\-*N\/A\-*|({db_query}[^=]+?))(\s\w+=|\s*$)""",
  """EVNTCLASSNAME=(\-*N\/A\-*|({db_object}[^=]+?))\s*\w+="""
  ]
  DupFields = ["event_name->db_operation"
}
```