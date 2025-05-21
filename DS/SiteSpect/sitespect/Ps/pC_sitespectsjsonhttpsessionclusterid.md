#### Parser Content
```Java
{
Name = sitespect-s-json-http-session-clusterid
  Vendor = SiteSpect
  Product = SiteSpect
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """cluster_id""","""user_guid""","""[SITESPECTBB_PROD]""","""[]""" ]
  Fields = [
    """\s({time}\d+-\d+-\d+T\d+:\d+:\d+).+?\s({host}[^\s]+)\s+({process_path}[^\s]+)""",
# processing_time is removed
    """url"+:"+(\/"+|({url}([^?";]+)((\?.+?)")?))""", #dl fields are removed
    """"+status"+:"+({http_response_code}\d+)"+""",
    """"+bytes"+:"+({bytes}\d+)"+""",
    """"+user_guid"+:"+({user_id}\d+)"+""",
# visit_count is removed
    """"+ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+""",
    """"+backend_ip"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"+method"+:"+({method}[^"]+)"+""",
    """"+user_agent"+:"+({user_agent}[^"]+)"+""",
    """"+http_referer"+:"+(-|({referrer}[^"]+))"+""",
    """"+pid"+:"+({process_id}\d+)"+""",
  ]


}
```