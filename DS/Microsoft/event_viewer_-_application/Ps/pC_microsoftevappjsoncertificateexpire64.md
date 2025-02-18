#### Parser Content
```Java
{
Name = microsoft-evapp-json-certificate-expire-64
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  Conditions = [ """"EventID":64,""", """Microsoft-Windows-CertificateServices""", """"Channel":"Application"""" ]
  DupFields = ["host -> src_host"]


}
```