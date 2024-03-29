#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-certificate-create-success-4887
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4887</EventID>""", """<Message>Certificate Services approved a certificate request and issued a certificate""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-events.Fields}[
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>""",
    """<Data Name ='Requester'>(({domain}[^<\\]+)\\)?({user}[^<]+)<""",
    """<Data Name ='Attributes'>\s*({attributes}[^<]+?)\s*<"""
    """<Data Name ='Disposition'>({disposition}[^<]+)""",
# subject_key is removed
    """<Data Name ='Subject'>({client_cert_subject}[^<]+)"""
  ]

xml-windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
  
}
```