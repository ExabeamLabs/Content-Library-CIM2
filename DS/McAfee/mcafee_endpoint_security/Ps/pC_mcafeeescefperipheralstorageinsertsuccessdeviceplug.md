#### Parser Content
```Java
{
Name = mcafee-es-cef-peripheral-storage-insert-success-deviceplug
        Vendor = McAfee
        Product = McAfee Endpoint Security
        TimeFormat = "epoch"
        Conditions = [ """|McAfee|DLPE|""", """ Device Plug|""" ]
        Fields = [
          """\Wcat=\s*Devices:\s*({operation}.+?)(\s+\w+=|\s*$)""",
          """\Wact=({action}.+?)(\s+\w+=|\s*$)""",
          """\Wmsg=({operation_details}.+?)(\s+\w+=|\s*$)""",
          """\Wrt=({time}\d{13})""",
          """\Wsuser=(({domain}[^\\]+)\\+)?({user}[^\\]+)(\s+\w+=|\s*$)""",
          """\Wsntdom=({domain}.+?)(\s+\w+=|\s*$)""",
          """\Wshost=({host}.+?)(\s+\w+=|\s*$)""",
          """\WfilePath=({file_path}.*?[\\\/]*({file_name}[^\\\/]*?))(\s+\w+=|\s*$)""",
          """\Wfsize=({bytes}\d+)""",
        ]
		ParserVersion = "v1.0.0"
    

}
```