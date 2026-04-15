#### Parser Content
```Java
{
Name = semperis-dsp-kv-security-alert-trigger
  ParserVersion = v1.0.0
  Vendor = Semperis
  Product = Semperis DSP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """Semperis.DSP""", """"Security indicator found":""", """"DSPLink":""", """"Security indicator name":""" ]
  Fields = [
    """"Generation time":"({time}[^"]+)"""
    """"ResultId":({result_code}\d+),"""
    """"Security indicator found":"({alert_description}[^"]+)"""
    """"Security indicator name":"({alert_name}[^"]+)"""
    """"Result":"({result}[^"]+)"""
    """"Target":"({target}[^"]+)"""
    """"Score":({risk_score}\d+),"""
    """"Severity":"({alert_severity}[^"]+)"""
    """"Security framework tags":"({technique}[^"]+)"""
    """"Result Message":"({additional_info}[^"]+)"""
    """"Number of results":({count}\d+)"""
    """"Remediation":"({remediation_steps}[^"]+)"""
    """"DSPLink":"({link}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"  


}
```