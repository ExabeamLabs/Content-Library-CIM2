#### Parser Content
```Java
{
Name = hp-nonstop-kv-app-activity-appactivity
Vendor = HP
Product = NonStop
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """ NONSTOP:""", """@""" ]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+)\.\d+[\+\-]\d+:\d+\s+({host}[^\s]+)\s+NONSTOP:.*?\@\s*\d+-\d+-\d+(:|\s+)\d+:\d+:\d+\.\d+([^@]*@){6}\s*({message_id_1}[^\s@]+)\s*@([^@]*@){4}\s*({message_id_2}[^@]+?)\s*@([^@]*@){4}\s*(|({object_1}[^@]+?))\s*@([^@]*@){2}\s*({object_2}[^@]+?)\s*@([^@]*@)\s*({message_id_3}[^@]+?)\s*@\s*(|({terminal}[^@]+?))\s*@([^@]*@){4}\s*({additional_info}[^@]+?)\s*(@|$)""",
]


}
```