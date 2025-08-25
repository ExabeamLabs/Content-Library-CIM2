# Code Changes for cef-defender-atp-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | full_name |  | ['"AccountName":"(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..AccountName,exa_regex=(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$.AccountName,exa_regex=(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['"AccountName":"(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..AccountName,exa_regex=(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$.AccountName,exa_regex=(-|NA|({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |