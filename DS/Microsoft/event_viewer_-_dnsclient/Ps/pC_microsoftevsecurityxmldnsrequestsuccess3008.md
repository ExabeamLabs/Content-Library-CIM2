#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-dns-request-success-3008"
  Vendor = "Microsoft"
  Product = "Event Viewer - DNSClient"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Conditions = [ """<EventID>3008<""", """Microsoft-Windows-DNS-Client""" ]
  Fields = [ 
    """Guid='\{({process_guid}[^}]+?)\}"""
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
    """<EventID>({event_code}\d+)</EventID>"""
    """<Task>({operation}.*?)</Task>"""
    """<Execution ProcessID\\*='({process_id}\d+)"""
    """<Computer>({dest_host}({host}[\w\-.]+?))</Computer>"""
    """<Data\s*Name =["']QueryType["']>({dns_query_type}[^<]+)<\/Data>""", 
    """<Data\s*Name =["']QueryName["']>({dns_query}[^<]+)<\/Data>""", 
  	"""<Data\s*Name =["']QueryResults["']>({dns_response}[^<]+)<\/Data>""", 
  	"""<Data\s*Name =["']QueryStatus["']>({result_code}[^<]+)<\/Data>"""
    """<Data\s*Name =["']QueryOptions["']>({dns_query_flags}[^<]+)<\/Data>"""
    """<Security UserID\\*='({user_sid}[^']+)'"""
    """<Keywords>({result}.+?)<\/Keywords>"""
    """<Level>({run_level}[^<]+)<"""
    """<Channel>({channel}[^<]+)<\/Channel>"""
    """ThreadID(\\)?=('|")({thread_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```