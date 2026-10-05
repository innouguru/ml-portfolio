# DNS Walkthrough

DNS stands for Domain Name System. It is responsible for resolving a domain name to the information needed to reach the service. The process involves several steps:

The client sends a request to the internet, and the DNS resolver takes the request and sends it to the root nameserver. The root nameserver tells the resolver which TLD nameserver serves the `.com`, `.net`, etc. The resolver then requests the TLD nameserver. The TLD nameserver tells the resolver which authoritative nameserver is responsible for the domain.

The resolver then queries the authoritative nameserver, which returns the relevant DNS record. The resolver sends this information back to the browser. The browser then uses the information from the DNS record to connect to the appropriate server and makes an HTTP request for the webpage.

For my website, I am using a Netlify-provided `*.netlify.app` domain, so I did not configure a custom domain or CNAME record myself.
