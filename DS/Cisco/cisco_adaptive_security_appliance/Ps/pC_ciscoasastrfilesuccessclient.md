#### Parser Content
```Java
{
Name = "cisco-asa-str-file-success-client"
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
    """, ApplicationProtocol:"""
    """, FileDirection: """
    """Client: """
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s+({host}[\w\-.]+)?\s*(\(|\%)"""
    """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """DstIP:\s*({web_domain}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """SrcPort:\s*({src_port}\d+)"""
    """DstPort:\s*({dest_port}\d+)"""
    """FileAction:\s*({action}[^,]+)"""
    """User:\s*(Unknown|({user}[^,\s]+))"""
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