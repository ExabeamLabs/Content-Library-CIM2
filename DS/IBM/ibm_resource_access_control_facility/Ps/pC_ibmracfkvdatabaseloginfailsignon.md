#### Parser Content
```Java
{
Name = ibm-racf-kv-database-login-fail-signon
  ParserVersion = v1.0.0
  Product = IBM Resource Access Control Facility
  Conditions = [ """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS""", """EVNTNAME=Signon""", """EVNTTIME=""", "EVNTDATE=""" ]
   DupFields = ${IBMracfParserTemplates.ibm-racf-activity.DupFields}["additional_info->reason"]

ibm-racf-activity = {
Vendor = IBM
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """APPLSIEMVRM=({host}[^=]+?)\s\w+=""",
  """APPLHOSTIPADD=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """EVNTUSERID=({db_user}[^=]+?)\s\w+=""",
  """EVNTNAME=({event_name}[^=]+?)\s\w+=""",
  """EVNTUSERNAME=(\-*N\/A\-*|({full_name}[^\s,]+(\s|,)[^=]+?)|({user}[^=\s]+?))\s\w+=""",
  """EVNTTEXT=({additional_info}[^=]+?)\s\w+=""",
  """EVNTCOMMAND=(\-*N\/A\-*|({db_query}[^=]+?))(\s\w+=|\s*$)""",
  """EVNTCLASSNAME=(\-*N\/A\-*|({db_object}[^=]+?))\s*\w+="""
  ]
  DupFields = ["event_name->db_operation"
}
```