#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-dll-load-moduleload
  ParserVersion = v1.0.0
  Conditions = [ """requestClientApplication=""" , """"type":"endpoint.event.moduleload"""", """destinationServiceName =""", """"process_username":"""", """"event_origin":"EDR"""" ]
  DupFields = ["process_name->src_process_name"]


}
```