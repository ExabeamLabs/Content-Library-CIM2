#### Parser Content
```Java
{
Name = "cisco-asa-str-file-success-client"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd yyyy HH:mm:ss"]
  Conditions = [
    """, ApplicationProtocol:"""
    """, FileDirection: """
    """Client: """
  ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)\s+(UTC\s+)?({host}[^\s]+)\s+:\s+%\w+\-""",
    """:\s*%\w+-\d+-({event_code}\d+)\s*:"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[\w\-.]+)?\s*(\(|\%|:)"""
    """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """SrcPort:\s*({src_port}\d+)"""
    """DstPort:\s*({dest_port}\d+)"""
    """FileAction:\s*({action}[^,]+)"""
    """User:\s*(Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """Client:\s*({user_agent}[^,]+)"""
    """Protocol:\s*({protocol}[^,]+)"""
    """FileSize:\s*({bytes}\d+)"""
    """FilePolicy:\s*({policy_name}[^,]+?)\s*,"""
    """FileDirection:\s*({direction}[^,]+)"""
    """FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({file_name}[^\\\/\",]+?(\.({file_ext}[^\\\/\.\s\",]+))?)))\s*,"""
  ]
  DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext" ]
  ParserVersion = "v1.0.0"


}
```