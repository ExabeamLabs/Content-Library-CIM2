#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-reset-success-30009
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>30009</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""" ]
  Fields = ${MicrosoftParserTemplates.account-password-activity-1.Fields}[
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
	"""<EventID>({event_code}30009)</EventID>"""
  ]
 
account-password-activity-1 = {
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Level>({run_level}[^<]+)<"""
    """<EventID>({event_code}\d+)</EventID>"""
    """<Correlation ActivityID\\*=('|")\{({activity_id}[^\}'"]+)"""
    """<Execution ProcessID=('|")({process_id}\d+)('|") ThreadID=('|")({thread_id}\d+)"""
    """<Channel>({channel}[^<]+)<\/Channel>"""
  
}
```