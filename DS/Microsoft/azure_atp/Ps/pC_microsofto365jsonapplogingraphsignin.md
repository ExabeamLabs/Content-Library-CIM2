#### Parser Content
```Java
{
Name = "microsoft-o365-json-app-login-graphsignin"
  ExtractionType = json
  Conditions = [ """"destinationServiceName":"Office 365"""", """"dproc":"Graph Sign-In logs"""", """failureReason":""" ]
  ParserVersion = "v1.0.0"

json-microsoft-security-events}{
Name = "microsoft-azureatp-json-alert-trigger-success-bruteforcesecurityalert"
ParserVersion = "v1.0.0"
Product = "Azure ATP"
Conditions = [""""category":"BruteForceSecurityAlert"""",""""title":""",""""vendor":""",""""Microsoft""""
}
```