#### Parser Content
```Java
{
Name = vmware-view-str-endpoint-delete-success-deleted
  ParserVersion = "v1.0.0"
  Conditions = [ """ View """, """has been deleted""" ]
  Fields = ${VMWareParsersTemplates.vmware-view-events.Fields}[
    """({operation}deleted)"""
   ]


}
```