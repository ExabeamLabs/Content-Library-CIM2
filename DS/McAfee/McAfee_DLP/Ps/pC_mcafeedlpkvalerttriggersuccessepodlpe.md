#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-epodlpe
	  ParserVersion = v1.0.0
      Vendor = McAfee
      Product = McAfee DLP
      TimeFormat = "epoch"
      Conditions = [ """|McAfee|DLPE|""", """|McAfee EPO DLPE""" ]
      Fields = [
        """\Wrt=({time}\d{13})""",
        """\Wshost=({host}[\w\-\.]+)\s*(\w+=|$)""",
        """\WeventId=({alert_id}\d+)""",
        """\Wcs1=({alert_type}.+?)\s*(\w+=|$)""",
        """\Wcat=({alert_name}.+?)\s*(\w+=|$)""",
        """\Wsuser=(({domain}[^\\]+)\\+)?({user}[^\\\s]+)\s*(\w+=[^\/]|$)""",
        """\Wsntdom=({domain}.+?)\s*(\w+=|$)""",
        """\Wfname=({file_name}[^,]+),\s*({target}.+?)\s*(\w+=|$)""",
        """\Wfsize=({bytes}\d+)\s*(\w+=|$)""",
        """\WrequestUrlHost=({dest_host}[\w\-\.]+)\s*(\w+=|$)""",
        """\|McAfee EPO DLPE.*?\|({alert_severity}[^\|]+)\|""",
        """\WcategoryOutcome=[\\\/]*({action}[^\\\/]+?)\s*(\w+=|$)""",
        """\Wsproc=({additional_info}.+?)\s*(\w+=|$)"""
      ]
    

}
```