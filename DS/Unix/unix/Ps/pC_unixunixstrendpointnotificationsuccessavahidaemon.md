#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-success-avahidaemon
  Conditions = [ """avahi-daemon[""", """]: Host name conflict""" ]
  Fields = ${DLUnixParserTemplates.unix-system-info.Fields}[
    """({event_name}Host name conflict)"""
  ]
  ParserVersion = "v1.0.0"

unix-system-info = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """(multipathd|avahi-daemon)\[\d+\]:(\ssda:)?\s({additional_info}[^"$]+?)\s*$"""
  
}
```