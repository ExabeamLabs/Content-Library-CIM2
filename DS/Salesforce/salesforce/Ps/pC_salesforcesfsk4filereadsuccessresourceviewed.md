#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-file-read-success-resourceviewed"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [
     """Resource: file"""
     """dproc="""
     """|resource-viewed|"""
     """destinationServiceName =Sales Cloud"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s+""",
    """\Wsuser=[^=]*?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-]{1,40}\$?)))""",
    """msg=({additional_info}[^=]+?)\s\w+="""
    """\WdestinationServiceName =({app}Sales Cloud)"""
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sfileType=({file_type}\w+)"""
    """\Wfname=(|({file_name}.+?(\.({file_ext}\w+))?))(\s+\w+=|\s*$)"""
    """IS_SUCCESS(\\)?=({result_code}[^";]+)"""
    """({operation}resource-viewed)"""
   ]
   DupFields = [
  "file_name->report"
   ]


}
```