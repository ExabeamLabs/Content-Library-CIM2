#### Parser Content
```Java
{
Name = microsoft-azure-sk4-app-file-success-secretget
  ParserVersion = v1.0.0
  Product = Azure Monitor
  Conditions= [ """destinationServiceName =Azure""", """dproc=Log Analytics OMS Workspace""", """"OperationName":"SecretGet"""", """"ResourceType":""" ]
  DupFields = [ "src_file_name->file_name" ]


}
```