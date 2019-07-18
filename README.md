Input: 
- ioc.txt

Processing: 
- Opens the IOC file, reads through each line and re-fangs the IOCs if they have been de-fanged
- Uses regex to look for IP addresses and add them to finalIPList
- Call curl_tld function to look for the TLD file or create a new one, then look for domains with those TLDs
- Use regex to look for hash values of types MD5, SHA1, or SHA256 and add matches to respective lists
- Add previous findings to fullList
- Create file IOCsearch_syntax.txt 

Output: 
- Send output of previously created lists to respective print functions and print RSA Netwitness formatted searches and Splunk searches, in addition to appending searches to IOCsearch_syntax.txt
- Finally, zip IOCsearch_syntax.txt
