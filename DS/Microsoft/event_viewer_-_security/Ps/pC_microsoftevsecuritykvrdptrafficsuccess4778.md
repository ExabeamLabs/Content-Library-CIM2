#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-rdp-traffic-success-4778"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd HH:mm:ss Z"]
  Conditions = [
    """A session was reconnected to a Window Station"""
    """Session Name"""
  ]
  Fields = [
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\s*(\+|\-)[\d\:]+)?)""""
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
    """({event_name}A session was reconnected to a Window Station)"""
    """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """\srt=({time}\d{13})"""
    """(?i)(((audit|success)( |_)(success|audit))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*"""
    """({host}[\w.\-]+)\s*:\s+A session was reconnected to a Window Station"""
    """({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4778\)"""
    """"dhn":"({host}[^-"]+)"""
    """<Computer>({host}[^<]+)</Computer>"""
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s|;)"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4778)"""
    """Account Name(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s;]*Account Domain(:|=)"""
    """Account Domain(:|=)(?:\\t|\\n|\\r|\s)*({domain}[^\s;]+?)[\s;]*(?:\\t|\\n|\\r|\s)*Logon ID(:|=)"""
    """\soriginalAgentHostName =({dest_host}[\w\-.]+?)\s+\w+="""
    """Service Name(:|=)\s*(::ffff:)?({dest_host}[\w\-.]+?)[\s;]*Service ID"""
    """(Client Address|src)(:|=)\s*(::[\w]+:)?(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """dst=\s*(::[\w]+:)?(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
    """Hostname":"({dest_host}[\w\-.]+?)""""
    """\sshost=({src_host}[\w\-.]+?)\s+\w+="""
    """Client Name(:|=)(\\r|\\t|\\n|\s)*({src_host}[\w\-\.]+)\s"""
    """ComputerName =({dest_host}[\w.\-]+)"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  ]
  ParserVersion = "v1.0.0"


}
```