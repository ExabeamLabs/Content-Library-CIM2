#### Parser Content
```Java
{
Name = goanywhere-gamft-kv-app-logout-success-disconnected
  ParserVersion = "v1.0.0"
  Conditions = [ """GoACHevent_type="Disconnect"""", """GoACHremote_ip="""", """GoACHcommand="Disconnect"""", """GoACHremarks="Disconnected"""" ]

goanywhere-dl-events-1 = {
    Vendor = GoAnywhere
    Product = GoAnywhere MFT
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)\s({dest_host}[\w\-.]+)""",
      """GoACHremote_ip="({src_ip}[\da-fA-F:\.]+)"""",
      """GoACHlocal_ip="({dest_ip}[\da-fA-F:\.]+)"""",
      """GoACHuser_name="(({email_address}[^@"]+@[^\.]+\.[^"]+)|(admin|666666|guest|({user}[^"]+)))"""",
      """GoACHevent_type="({event_name}[^"]+)"""",
    
}
```