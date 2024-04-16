#### Parser Content
```Java
{
Name = a-avi-str-endpoint-notification-success-ipreputationdbsyncfailure
 ParserVersion = "v1.0.0"
 Conditions= [ """Avi-Controller""", """event IP_REPUTATION_DB_SYNC_FAILURE""", """Failed""" ]
 
nsx-config-endpoint-notification-success = {
    Vendor = AVI Networks
    Product = AVI Networks Software Load Balancer
    TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
    Fields = [
      """({host}[\w\-\.]+)\sAvi-Controller""",
      """event\s({event_name}[^\s]+)""",
      """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d.\d\d:\d\d)\sevent""",
      """({result}Success|Failed)""",
      """tenant\s({tenant}[\w\-\.]+)\s"""
    
}
```