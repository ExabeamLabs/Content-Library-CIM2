#### Parser Content
```Java
{
Name = mcafee-es-cef-peripheral-storage-insert-success-deviceplug
        Vendor = Trellix
        Product = Trellix Endpoint Security
        TimeFormat = "epoch"
        Conditions = [ """|McAfee|DLPE|""", """ Device Plug|""" ]
        Fields = [
          """\Wcat=\s*Devices:\s*({operation}.+?)(\s+\w+=|\s*$)""",
          """\Wact=({action}.+?)(\s+\w+=|\s*$)""",
          """\Wmsg=({operation_details}.+?)(\s+\w+=|\s*$)""",
          """\Wrt=({time}\d{13})""",
          """\Wsuser=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)""",
          """\Wsntdom=({domain}.+?)(\s+\w+=|\s*$)""",
          """\Wshost=({host}.+?)(\s+\w+=|\s*$)""",
          """\WfilePath=({file_path}.*?[\\\/]*({file_name}[^\\\/]*?))(\s+\w+=|\s*$)""",
          """\Wfsize=({bytes}\d+)""",
          """"INSTANCE_ID">USB\\\\VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)"""
        ]
		ParserVersion = "v1.0.0"
    

}
```