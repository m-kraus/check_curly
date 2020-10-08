# About check_curly

check_curly is a plugin for nagios and similar monitoring tools like icinga, naemon or shinken.  

PHP with CURL-extension needs to be installed. Depending on your distribution, different packages ar required.
On Redhat RHEL or CentOS for example install the following packages:

    yum install php-common php-cli

On Debian or Ubuntu install those packages:

    apt-get install php5-cli php5-curl


## Help

    ./check_curly --help
    
    check_curly
    Originally written by Vit Safar, extended by Michael Kraus
    
     Syntax:
        -u URL [http(s)://URL(:PORT)]
        -c Critical page return time in seconds [TIME]
        -w Warning page return time in seconds [TIME]
        -t Plugin timeout in seconds (default 10) [TIME]
    
        -f Follow redirects
        -k Ignore SSL certificate errors
    
        -e Expected HTTP response code [HTTP_RESPONSE_CODE[,HTTP_RESPONSE_CODE,...]]
    
        --proxy Proxy [http://PROXY:PORT]
        --agent Agent [USER_AGENT]
           (default Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; Trident/6.0))
        --ntlm Set NTLM auth credentials [USER:PASSWORD]
    
        -g Find string on page [STRING]
    
        --sizebelowcritical Critical below page size in bytes [SIZE]
        --sizeovercritical Critical over page size in bytes [SIZE]
        --sizebelowwarning Warning below page size in bytes [SIZE]
        --sizeoverwarning Warning over page size in bytes [SIZE]
    
        --showheaders Show page headers
        --showbody Show page body
        --noperfdata Exclude performance data
    
        --nullcookiejar Set cookie jar to /dev/null (workaround to prevent infinite loop when redirecting)
    
        --alias Alternative text to be included in plugin output
    
        --debug Enable debug mode
    
     Example:
      check_curly -u http://test.example.net
