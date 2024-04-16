#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-success-sfcbd
  ParserVersion = v1.0.0
  Conditions = [ """ sfcbd[""", """]: """ ]

VMParserTemplates}{
  Name = vmware-esxi-str-endpoint-activity-vmkernel
  ParserVersion = v1.0.0
  Conditions = [ """vmkernel:""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Last path removed for TGT)"""
    
}
```