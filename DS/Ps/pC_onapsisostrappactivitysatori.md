#### Parser Content
```Java
{
Name = onapsis-o-str-app-activity-satori
    Vendor=Onapsis
    Product=Onapsis 
    ParserVersion = "v1.0.0"
    TimeFormat="yyyy-MM-dd HH:mm:ss"
    Conditions=[ """ onapcon """, """  [satori"""  ]
    Fields=[
      """({host}onapcon)""",
      """onapcon\s({severity}[^\s]+)""",
# compliance_job is removed
      """owner=\s*"(u:)?({user}[\w\.\-]{1,40}\$?)""",
      """\[satori.+?\]\s+\S+\s+({additional_info}.+?)[\s.]*$"""
]


}
```