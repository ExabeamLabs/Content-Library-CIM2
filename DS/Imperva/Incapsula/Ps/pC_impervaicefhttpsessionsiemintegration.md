#### Parser Content
```Java
{
Name = imperva-i-cef-http-session-siemintegration
  ParserVersion = v1.0.0  
  Vendor = Imperva
  Product = Incapsula
  TimeFormat = "epoch"
  Conditions = [ 
"""CEF:"""
"""|Incapsula|SIEMintegration|"""
"""deviceExternalId"""
""" ccode"""
]
  Fields = [
        """sip\\=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s""",
        """start\\=({time}\d+)""",
        """src\\=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s""",
        """sourceServiceName\\=({web_domain}.+?)\s+(\w+=|$)""",
        """act\\=({action}[A-Z_]+)\s""",
        """requestClientApplication\\=({user_agent}.+?)\s+(\w+\\=|$)""",
        """cn1\\=({http_response_code}\d+)\s""",
        """cpt\\=({src_port}\d+)\s""",
        """spt\\=({dest_port}\d+)\s""",
        """app\\=({protocol}[^|\s]+)\s""",
        """request\\=({uri_path}[^\s]+)\s""",
        """qstr\\=({uri_query}[^|]+)\\\\=""",
        """in\\=({bytes}\d+|$)\s""",
  ]

  DupFields = [ "uri_path->url" ]


}
```