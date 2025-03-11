#### Parser Content
```Java
{
Name = netapp-n-sk4-file-permission-modify-4670
  ParserVersion = "v1.0.0"
  Conditions = [ """'NetApp-Security-Auditing'""", """EventID': 4670""", """'Permissions Changed'"""  ]
  Fields = ${DLWindowsParsersTemplates.netapp-json-windows-events.Fields}[
    """'Computer':\s+'({host}[\w\-\.]+)"""
  ]


}
```