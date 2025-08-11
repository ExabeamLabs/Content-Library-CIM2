#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-certificate-modify-success-5126
   Vendor = Microsoft
   Product = Event Viewer - Security
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
   Conditions = ["""<EventID>5126</EventID>""",  """Microsoft-Windows-Security-Auditing""" ]
   Fields = [
     """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """<EventID>({event_code}\d+)""",
     """<Computer>({host}[^<]+)""",
     """<Level>({run_level}[^<]+)<"""
     """<Data Name =('|")NewSigningCertificateHash('|")>({hash_sha1}[^<]+)"""
     """<Data Name =('|")CAConfigurationId('|")>({activity_id}[^<]+)"""
   ]


}
```