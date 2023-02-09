#### Parser Content
```Java
{
Name = zeek-z-json-file-success-sbmfiles
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"id.orig_h""", """"id.resp_h""", """"action""", """"smb_files""" ]
  Fields = [
    """"HOST":\s*"({host}[^"]+)"""",
    """"TAGS":\s*"({event_code}[^"]+)"""",
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""",
    """SMB::({access}\w+)""",
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"path":"({share_path}[^"]+)"""",
    """"name":"({src_file_path}({file_dir}[^"]*?(\\u005c))?({src_file_name}[^"\\\/]*?(\.({src_file_ext}\w+))?))"""",
  ]
  DupFields = [ "src_file_name->file_name" ]


}
```