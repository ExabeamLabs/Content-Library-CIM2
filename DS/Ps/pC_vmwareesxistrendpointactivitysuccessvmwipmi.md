#### Parser Content
```Java
{
Name = vmware-esxi-str-endpoint-activity-success-vmwipmi
  Conditions = [ """ sfcb-vmw_ipmi[""", """]: """ ]
  ParserVersion = "v1.0.0"

VMParserTemplates}{
  Name = vmware-esxi-str-endpoint-activity-vmkernel
  ParserVersion = v1.0.0
  Conditions = [ """vmkernel:""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Last path removed for TGT)"""
    
}
```