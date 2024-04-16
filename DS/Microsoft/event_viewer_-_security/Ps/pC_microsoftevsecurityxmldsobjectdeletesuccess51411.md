#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-ds-object-delete-success-5141-1
  ParserVersion = v1.0.0
  Conditions = [  """"Activity":"5141 - A directory service object was deleted."""", """"EventID":5141""", """"EventSourceName":"Microsoft-Windows-Security-Auditing""""]
  Fields = ${WindowsParsersTemplates.json-windows-events-4.Fields}[
    """<Data Name\\?=\\?"ObjectDN\\?">(|({ds_object_dn}[^<]+))<\/Data>""",
    """<Data Name\\?=\\?"ObjectClass\\?">(|({ds_object_class}[^<]+))<\/Data>""",
    """<Data Name\\?=\\?"SubjectUserSid\\?">({user_sid}[^<]+)<\/Data>""",
    """<Data Name\\?=\\?"SubjectUserName\\?">({user}[\w\.\-]{1,40}\$?)<\/Data>""",
    """<Data Name\\?=\\?"SubjectDomainName\\?">({domain}[^<]+)<\/Data>""",
    """<Data Name\\?=\\?"SubjectLogonId\\?">({login_id}[^<]+)<\/Data>"""
  ]

json-windows-events-4 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
    """"Computer":"({host}[\w\-\.]+)"""",
    """"EventID":({event_code}\d+),""",
    """"Activity":"\d+\s\-\s({event_name}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```