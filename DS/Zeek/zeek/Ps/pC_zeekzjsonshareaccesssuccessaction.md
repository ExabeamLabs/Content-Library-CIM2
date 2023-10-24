#### Parser Content
```Java
{
Name = "zeek-z-json-share-access-success-action"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """"id.orig_h"""
  """"id.resp_h"""
  """"action"""
  """"SMB::FILE_OPEN"""
]
Fields = [
  """"HOST\"+:\s*\"+({host}[^\"]+)\""""
  """"TAGS\"+:\s*\"+({event_code}[^\"]+)\""""
  """"ts\\?\"+:\\?\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
  """SMB::({access}FILE_OPEN)"""
  """"id\.orig_h\\?\"+:\\?\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"id\.orig_p\\?\"+:({src_port}\d+)"""
  """"id\.resp_h\\?\"+:\\?\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"id\.resp_p\\?\"+:({dest_port}\d+)"""
  """"path\\?\"+:\\?\"+({share_path}[^\"]+)"""
  """"name\\?\"+:\\?\"+({file_path}({file_dir}[^\"]*?(\\u005c|[\\\/])*)({file_name}[^\"\\\/]+?(\.({file_ext}[^\"\\\/\.]+))?))\s*\\?\""""
  """"size\\?\"+:({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```