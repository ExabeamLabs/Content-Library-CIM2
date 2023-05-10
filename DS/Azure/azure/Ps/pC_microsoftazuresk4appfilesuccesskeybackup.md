#### Parser Content
```Java
{
Name = microsoft-azure-sk4-app-file-success-keybackup
  ParserVersion = v1.0.0
  Product = Azure
  Conditions= [ """destinationServiceName =Azure""", """dproc=Log Analytics OMS Workspace""", """"OperationName":"KeyBackup"""", """"ResourceType":""" ]
  DupFields = [ "src_file_name->file_name" ]


}
```