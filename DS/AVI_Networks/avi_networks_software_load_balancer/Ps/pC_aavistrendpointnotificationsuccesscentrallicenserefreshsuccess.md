#### Parser Content
```Java
{
Name = a-avi-str-endpoint-notification-success-centrallicenserefreshsuccess
 ParserVersion = "v1.0.0"
 Conditions= [ """Avi-Controller""", """event CENTRAL_LICENSE_REFRESH_SUCCESS""", """INFO""" ]
 
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