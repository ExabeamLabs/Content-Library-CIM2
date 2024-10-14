#### Parser Content
```Java
{
Name = microsoft-evadfs-xml-ds-object-create-success-4928
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """<EventID>4928</EventID>""", """<Execution ProcessID""", """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """({event_code}4928)""",
    """<Data Name\\*=('|")DestinationDRA('|")>({ds_object_dn}CN=.*?DC=.*?)</Data>""",
    """<Data Name\\*=('|")SourceDRA('|")>({src_ds_object_dn}CN=.*?DC=.*?)</Data>""",
    """<Data Name\\*=('|")SourceAddr('|")>({src_host}[\w\-.]+)</Data>""",
    """<Data Name\\*=('|")NamingContext('|")>({naming_context}[^\s]+)</Data>""",
    """<Data Name\\*=('|")Options('|")>({options}\d+)</Data>""",
    """<Data Name\\*=('|")StatusCode('|")>({result_code}\d+)</Data>""",
     ]
  

}
```