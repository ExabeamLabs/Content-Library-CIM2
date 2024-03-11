#### Parser Content
```Java
{
Name = goanywhere-gamft-kv-file-upload-success-upload
  Conditions = [ """GoAnywhereServicesevent_type="Upload Successful"""","""GoAnywhereServicescommand="Upload""","""GoAnywhereServicesremote_ip="""" ]
  Fields = ${GoAnywhereParsersTemplates.goanywhere-events.Fields}[
     """GoAnywhereServicesvirtual_path="({file_path}[^"]*\/({file_name}[^"]*))"""",
     """"({operation}Upload)""""
  ]
  ParserVersion = v1.0.0

goanywhere-events = {
    Vendor = GoAnywhere
    Product = GoAnywhere MFT
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)\s({dest_host}[\w\-.]+)""",
      """GoAnywhereServiceslocal_ip="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """GoAnywhereServicesremote_ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """GoAnywhereServicesuser_name="(({email_address}[^@"]+@[^\.]+\.[^"]+)|(admin|666666|guest|({user}[^"]+)))"""",
      """GoAnywhereServicesevent_type="({event_name}[^"]+)"""",
    
}
```