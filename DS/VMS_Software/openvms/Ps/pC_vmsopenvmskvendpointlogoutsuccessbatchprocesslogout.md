#### Parser Content
```Java
{
Name = vms-openvms-kv-endpoint-logout-success-batchprocesslogout
  ParserVersion = "v1.0.0"
  Conditions = [ """Auditable event:""", """Batch process logout""", """Username:""" ]
  Fields = ${OpenVMSDLParserTemplates.openvms-logout.Fields}[
    """({event_name}Batch process logout)"""
  ]
   DupFields = [ "event_name->operation" ]

openvms-logout = {
  Vendor = VMS Software
  Product = OpenVMS
  TimeFormat = "dd-MMM-yyyy HH:mm:ss.SS"
  Fields = [
    """Event time:\s+({time}\d\d-\w+-\d\d\d\d\s+\d\d:\d\d:\d\d\.\d\d)""",
    """Username:\s+({user}[^\s]+)\s+(\w+|$)""",
    """PID:\s+({process_id}[\w]+)\s+(\w+|$)""",
    """Process name:\s+({process_name}[^\s]+)\s+(\w+|$)""",                                            
}
```