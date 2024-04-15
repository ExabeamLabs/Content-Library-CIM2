#### Parser Content
```Java
{
Name = "netdoc-n-json-file-activity-success"
Product = "NetDocs"
Vendor = "NetDocs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""memberType": """
"""storageObject":"""
"""cabinet": """
]
Fields = [
""""+host"+:\s"+({host}[^"]+)"+,"""
""""+host"+:\s"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+,"""
"""date"+:\s"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""+date"+:\s+"+({time}[^"]+)"+"""
""""+user.+?"+name"+:\s+"+({full_name}[^"]+)"+\}?,"""
""""+memberType.+?"+id"+:\s+"+({user_id}[^"]+)"""
""""+fileExtension"+:\s+"+({file_ext}[^"]+)"""
""""+size"+:\s+"+({bytes}\d+)"""
""""+memberType"+:\s+"+({object}[^"]+)"""
""""+cabinet".+?id"+:\s+"+({dest_host}[^"]+)"""
""""+name"+: "+({operation}[^"]+)"+}}"*"""
"""name"+:\s+"+({operation}[^"]+)"+,\s+"+(date|source|storageObject|host)"""
"""activity"+:\s+\{"+name"+:\s+"+({operation}[^"]+)"""
""""+CorpMatter"+:\s+"+({corp_matter}[^"]+)"+"""
""""+CorpClient"+:\s+"+({corp_client}[^"]+)"+"""
""""+cabinet"+:.+?name"+:\s"+({cabinet_name}[^"]+)"""
"""name"+:\s+"+({src_file_name}[^"]+)"+,?\s+"+(TypeofEngagement|DocumentType|OfficeofAuthor)"""
""""+docId"+:\s+"+({doc_id}[^"]+)"""
"""activity"+:\s+\{"+name"+:\s+"+({operation}[^"]+)"""
""""access"+:\s+"+({additional_info}[^"]+)"""
"""name"+:\s+"+({src_file_name}[^"]+)"+,\s+"+(TypeofEngagement|DocumentType|OfficeofAuthor|Author|fileExtension|size)"""
"""name"+:\s+"+({src_file_name}[^"]+)"+}?,\s+"+(user|CorpClient|version|Client)"""
"""(docId|Author|DocumentType)"+:\s+"+[^"]+"+,\s+"+name"+:\s+"+({src_file_name}[^"]+)"""
"""({app}netdocs)"""
]
DupFields = [
"operation->access"
]
ParserVersion = "v1.0.0"


}
```