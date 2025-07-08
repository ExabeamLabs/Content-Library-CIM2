# Code Changes for json-aws-guardduty-security-alert-template (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tags | ['"tags":\[({tags}.+"\})\]\}'] | ['"tags":\s*({tags}[^$]+?)\]', 'exa_regex="tags":\s*({tags}[^$]+?)\]'] |