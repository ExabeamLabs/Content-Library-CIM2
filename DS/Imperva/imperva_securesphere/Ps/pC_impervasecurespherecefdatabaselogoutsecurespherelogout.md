#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-logout-securespherelogout
  Vendor = Imperva 
  Product = Imperva SecureSphere
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Imperva Inc.|SecureSphere|""", """cs6=Logout""" ]
  Fields = [
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wduser=(|(({domain}[^\\]+)\\)?({db_user}[^\\]+?))(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wproto=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)""",
    """\Wcat=(|({category}.+?))(\s+\w+=|\s*$)""",
    """\Wcs2=(|({server_group}.+?))(\s+\w+=|\s*$)""",
    """\Wcs3=(|({service_name}.+?))(\s+\w+=|\s*$)""",
    """\Wcs4=(|({app}.+?))(\s+\w+=|\s*$)""",
# user_authenticated is removed
    """\Wcs11=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\Wcs12=(({domain}[^\\\s]+)\\+)?({host}[\w\-.]+)""",
    """\Wcs13=(|({db_name}.+?))(\s+\w+=|\s*$)""",
    """\Wcs14=(|({db_schema}.+?))(\s+\w+=|\s*$)"""
  ]
  DupFields = [ "db_user->account" ]
  ParserVersion = "v1.0.0"


}
```