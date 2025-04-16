#### Parser Content
```Java
{
Name = netapp-n-sk4-file-rename-9999
  ParserVersion = "v1.0.0"
  Conditions = [  """'NetApp-Security-Auditing'""", """'EventID': 9999""", """'Rename"""  ]
  Fields = ${DLWindowsParsersTemplates.netapp-json-windows-events.Fields}[
    """'Computer':\s+'({host}[\w\-\.]+)"""
  ]
  DupFields = ["src_user->user", "src_domain->domain"]


}
```