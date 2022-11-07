#### Parser Content
```Java
{
Name = goanywhere-gamft-kv-file-download-success-download
  Conditions = [ """GoAnywhereServicesevent_type="Download Successful"""","""GoAnywhereServicescommand="Download"""","""GoAnywhereServicesremote_ip="""" ]
  Fields = ${GoAnywhereParsersTemplates.goanywhere-events.Fields}[
     """GoAnywhereServicesvirtual_path="({file_path}[^"]*\/({file_name}[^"]*))"""",
     """"({operation}Download)""""
  ]
  ParserVersion = v1.0.0

goanywhere-events = {
    Vendor = GoAnywhere
    Product = GoAnywhere MFT
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)\s({dest_host}[\w\-.]+)""",
      """GoAnywhereServiceslocal_ip="({dest_ip}[A-Fa-f\d.:]+)"""",
      """GoAnywhereServicesremote_ip="({src_ip}[A-Fa-f\d.:]+)"""",
      """GoAnywhereServicesuser_name="(({email_address}[^@"]+@[^\.]+\.[^"]+)|(admin|666666|guest|({user}[^"]+)))"""",
      """GoAnywhereServicesevent_type="({event_name}[^"]+)"""",
    
}
```