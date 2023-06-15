#### Parser Content
```Java
{
Name = goanywhere-gamft-kv-file-rename-fail-failed
  ParserVersion = "v1.0.0"
  Conditions = [ """GoAnywhereServicesevent_type="Rename File Failed"""","""GoAnywhereServicesremote_ip="""" ]
  Fields = ${GoAnywhereParsersDLTemplates.goanywhere-dl-events.Fields}[
    """GoAnywhereServicesfile_path="\w+\:\\+\w+\\+\w+\\+\w+\\+\w+\\+({old_file_name}[^"]+)"""
  ]
  DupFields = [ "event_name->failure_reason" , "old_file_name -> file_name"]

goanywhere-dl-events = {
    Vendor = GoAnywhere
    Product = GoAnywhere MFT
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)\s({dest_host}[\w\-.]+)""",
      """GoAnywhereServiceslocal_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """GoAnywhereServicesremote_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """GoAnywhereServicesuser_name="(({email_address}[^@"]+@[^\.]+\.[^"]+)|(admin|666666|guest|({user}[^"]+)))"""",
      """GoAnywhereServicesevent_type="({event_name}[^"]+)"""",
    
}
```