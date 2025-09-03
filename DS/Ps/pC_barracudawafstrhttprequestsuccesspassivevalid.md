#### Parser Content
```Java
{
Name = barracuda-waf-str-http-request-success-passivevalid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER""", """ PROFILED""", """PASSIVE""" ]

barracuda-web-activity}{
  Name = barracuda-waf-str-http-request-success-profiledvalid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER""", """PROFILED""", """PROTECTED""", """VALID""" 
}
```