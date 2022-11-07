#### Parser Content
```Java
{
Name = goanywhere-gamft-kv-file-delete-success-deletefile-1
  Conditions = [ """GoACHevent_type="Delete File Successful"""", """GoACHcommand="Delete"""", """GoACHremote_ip="""", """GoACHuser_name="""" ]
  Fields = ${GoAnywhereParsersTemplates.goanywhere-events-2.Fields}[
     """GoACHfile_path="({file_path}[^"]*\/({file_name}[^"]*))"""",
     """"({operation}Delete)""""
  ]
  ParserVersion = v1.0.0

goanywhere-events-2 = {
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