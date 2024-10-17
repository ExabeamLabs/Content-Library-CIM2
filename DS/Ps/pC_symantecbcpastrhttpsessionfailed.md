#### Parser Content
```Java
{
Name = "symantec-bcpa-str-http-session-failed"
  ParserVersion = "v1.0.0"
  Conditions = [ """PROXIED""", """ ssl """]

bluecoat-proxy}{
  Name = "symantec-bcpa-mix-http-session-proxied"
  ParserVersion = "v1.0.0"
  Conditions = [ """ PROXIED """, """http""" 
}
```