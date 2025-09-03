#### Parser Content
```Java
{
Name = "microsoft-o365-json-app-login-graphsignin"
  ExtractionType = json
  Conditions = [ """"destinationServiceName":"Office 365"""", """"dproc":"Graph Sign-In logs"""", """failureReason":""" ]
  ParserVersion = "v1.0.0"
  DupFields = ["event_name->operation"]


}
```