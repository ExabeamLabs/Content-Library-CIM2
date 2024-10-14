#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-4673"
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = ["CEF:", "|Snare|", "|A privileged service was called", "Microsoft-Windows-Security-Auditing:4673|"]
  Fields = [
    """({event_name}A privileged service was called)""",
    """\srt=({time}\d{13})""",
    """\s(deviceSeverity|severity)=({result}[^\s]+)""",
    """\sdhost=({host}[\w\-.]+?)(\s+[^\s]+=|\s*$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """({event_code}4673)""",
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[^\s]+=|\s*$)""",
    """\sdntdom=({domain}.+?)(\s+[^\s]+=|\s*$)""",
    """\sad.Service:Server=({object_server}.+?)(\s+[^\s]+=|\s*$)""",
    """\sduid=({login_id}[^\s]+)""",
    """(\s|:)Privileges(:|=)\s*({privileges}.+?)(\s+[^\s]+(=|:)|\s*$)""",
    """Process Name(:|=)\s*(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Service Request Information(:|=)""",
    """\s*Account Name(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s;]*Account Domain(:|=)""",
    """\s*Account Domain(:|=)\s*({domain}.+?)[\s;]*Logon ID(:|=)""",
    """\s*Logon ID(:|=)\s*({login_id}.+?)[\s;]*Service(:|=)""",
    """\s*Server(:|=)\s*({object_server}.+?)[\s;]*Service Name""",
  ]
  DupFields = ["host->dest_host"]


}
```