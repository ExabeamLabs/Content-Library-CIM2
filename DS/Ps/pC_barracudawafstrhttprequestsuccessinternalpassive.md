#### Parser Content
```Java
{
Name = barracuda-waf-str-http-request-success-internalpassive
  ParserVersion = v1.0.0
  Conditions = [ """INTERNAL""", """PASSIVE""" ]

barracuda-web-activity}{
  Name = barracuda-waf-str-http-request-success-profiledvalid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER""", """PROFILED""", """PROTECTED""", """VALID""" 
}
```