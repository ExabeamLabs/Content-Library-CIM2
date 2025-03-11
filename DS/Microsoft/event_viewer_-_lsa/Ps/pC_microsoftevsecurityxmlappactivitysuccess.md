#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-activity-success
  Product = "Event Viewer - LSA"
  Conditions = [ """<Channel>Microsoft-Windows-LSA""", """<EventID>300</EventID>""", """<Computer>""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-xml-events.Fields}[
    """Data Name(\\)?=('|")TargetUserName('|")>({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
    """Data Name(\\)?=('|")TargetDomainName('|")>({dest_domain}[^<]+)"""
    """Data Name(\\)?=('|")TargetLogonId('|")>({dest_login_id}[^<]+)"""
    """Data Name(\\)?=('|")TargetUserSid('|")>({dest_user_sid}[^<]+)"""
  ]
  DupFields = [ "dest_user->user","dest_user_sid->user_sid","dest_domain->domain","dest_login_id->login_id"]

windows-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID='({user_sid}[^']+)'\/>""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name ='({provider_name}[^']+)'""",
    """Guid='\{({process_guid}[^}]+?)\}""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```