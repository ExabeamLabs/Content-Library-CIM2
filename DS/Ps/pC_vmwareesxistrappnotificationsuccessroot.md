#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-success-root
  ParserVersion = v1.0.0
  Conditions = [ """ root[""", """]: """ ]

VMParserTemplates}{
  Name = vmware-esxi-str-endpoint-activity-vmkernel
  ParserVersion = v1.0.0
  Conditions = [ """vmkernel:""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Last path removed for TGT)"""
    
}
```