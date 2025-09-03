#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-send-workload
  ParserVersion = v1.0.0
  Conditions = [
    """Workload""",
    """ClientProcessName""",
    """Subject""",
    """"SendOnBehalf""""
  ]
 }, 
${MicrosoftAzureParsersTemplates.o365-dlp-email-out} {
  Name = microsoft-o365-cef-email-send-sendas
  ParserVersion = v1.0.0
  Conditions = [
    """Workload""",
    """ClientProcessName""",
    """Subject""",
    """"SendAs"""
  ]
 

}
```