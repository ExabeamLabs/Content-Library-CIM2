#### Parser Content
```Java
{
Name = vms-openvms-kv-endpoint-logout-success-remoteinteractivelogout
  ParserVersion = "v1.0.0"
  Conditions = [ """Auditable event:""", """Remote interactive logout""", """Username:""" ]
  Fields = ${OpenVMSDLParserTemplates.openvms-logout.Fields}[
    """Terminal name:\s+({additional_info}[^\s]+)\s+(\w+|$)""",
    """Host:\s+({host}[A-Fa-f\d\.:]+)\s+(\w+|$)""",
    """({event_name}Remote interactive logout)"""
  ]
  DupFields = [ "event_name->operation","host->dest_ip" ]

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