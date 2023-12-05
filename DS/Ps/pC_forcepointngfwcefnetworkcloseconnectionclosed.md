#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-close-connectionclosed
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|FORCEPOINT|""", """|Connection_Closed|""" ]
  Fields = ${DLForcepointParsersTemplates.forcepoint-template.Fields} [
    ]


}
```