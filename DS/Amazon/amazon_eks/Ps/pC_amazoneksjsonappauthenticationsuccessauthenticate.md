#### Parser Content
```Java
{
Name = amazon-eks-json-app-authentication-success-authenticate
    Product = Amazon EKS
    Vendor = Amazon
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [
      """authenticator""",
      """msg="""",
      """eks"""
      ]
      Fields =[
      """"*username\\?"*(=>|:|=)\\?"*({user}[\w\.\-]{1,40}\$?)""",
      """"*groups\\?"*(=>|:|=)"\[\\?({group_name}[^"\\\]]+)""",
      """({time}\d+\-\d+\-\d+T\d\d:\d\d:\d\dZ)""",
      """"AccountName":"({account}[^"\\]+)""""
      """"logStream":"({service_name}[^"]+)""""
      """"owner":"({owner_id}[^"]+)""""
      ]
    ParserVersion = "v1.0.0"


}
```