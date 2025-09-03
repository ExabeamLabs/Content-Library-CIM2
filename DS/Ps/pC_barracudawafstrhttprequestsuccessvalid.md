#### Parser Content
```Java
{
Name = barracuda-waf-str-http-request-success-valid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER""", """DEFAULT""", """PROTECTED""" ]

barracuda-web-activity}{
  Name = barracuda-waf-str-http-request-success-profiledvalid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER""", """PROFILED""", """PROTECTED""", """VALID""" 
}
```