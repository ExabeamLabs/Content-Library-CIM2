#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-certificate-create-success-4887
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["epoch", "MMM dd HH:mm:ss"]
  ParserVersion = v1.0.0
  Conditions = [ """"Id":4887""", """"ProviderName":""", """Microsoft-Windows-Security-Auditing""", """Certificate Services approved a certificate request""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)\s"""
    """"Id":({event_code}\d+)"""
    """"Task":({task_id}\d+)"""
    """"ProviderName":"({provider_name}[^"]+)""""
    """"ProcessId":({process_id}\d+)"""
    """"ThreadId":({thread_id}\d+)"""
    """"MachineName":"({host}[^"]+)""""
    """"TimeCreated":"[^\(]+\(({time}\d{13})\)"""
    """"OpcodeDisplayName":"({opcode}[^"]+)""""
    """"TaskDisplayName":"({task_name}[^"]+)""""
    """"KeywordsDisplayNames":\[?"({result}[^"]+)""""
    """"Message":"({event_name}[^"\.]+)"""
    """Requester:(({domain}[^<\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """"LevelDisplayName":"({run_level}[^"]+)""""
    """\sDisposition:({disposition}\d+)"""
    """\sSubject:CN=({client_cert_subject}[^"\}]+)"""
    """CertificateTemplate:\s*({additional_info}[^\s:]+?)(\\n)?\s*\w+:"""
  ]


}
```