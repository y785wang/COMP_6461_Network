On terminal, use 'javac httpc.java' to compile

Command line basic test cases

Help
    java httpc
    java httpc help
    java httpc help get
    java httpc help post

Get
    java httpc get 'http://httpbin.org/get'
    java httpc get 'http://httpbin.org/get?course=networking&assignment=1' -v -h 123:123
    
Post
    java httpc post 'http://httpbin.org/post'
    java httpc post 'http://httpbin.org/post' -v -h 123:123 -d 456
    java httpc post 'http://httpbin.org/post' -v -h 123:123 -f input -o output
    java httpc post 'http://httpbin.org/post' -v -h 123:123 -d 456 -f input

Redirect code302:
    java httpc get  http://httpbin.org/redirect/n -v -h 123:123
    java httpc get  http://httpbin.org/absolute-redirect/n -v -h 123:123
    java httpc get  http://httpbin.org/redirect-to?url=http://httpbin.org/get -v -h 123:123
    java httpc post http://httpbin.org/redirect-to?url=http://httpbin.org/post -v -h 123:123 -d 456
    java httpc post http://httpbin.org/redirect-to?url=http://httpbin.org/post -v -h 123:123 -f input -o output

Note:
    1) n is any positive integer
    2) Set variable 'seeRedirectDetail = false' at the top of the sendRequest class (line 139 of http.java) to hide the redirect detail, default is true
    3) -v and -h commands support duplicate, -d and -f do not support duplicate