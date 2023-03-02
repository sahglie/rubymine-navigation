# README

This project demonstrates how rubymine is unable to correctly navigate between 
test and implementation. After running `rails new rubymine-navigation` I added
the following files:

```
#{Rails.root}/models/event.rb
#{Rails.root}/models/ids/event.rb
#{Rails.root}/lib/suricata/event.rb


#{Rails.root}/test/models/event.rb
#{Rails.root}/test/models/ids/event.rb
#{Rails.root}/test/lib/suricata/event.rb
```

If I am within any non-test file and I run `navigate to test` rubymine opens a
drop down and lists all of the test files. It doesn't even try to match things
or give preference to the test file that corresponds to the file I am in.

Expected behaviour would be that if there is a test file that corresponds exactly
to a standard file, then that file should be opened. It should only show me a list
of file if there is no exact match.
