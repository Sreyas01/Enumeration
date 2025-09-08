# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

| Operator    | Description                        | Example Usage           |
| ----------- | ---------------------------------- | ----------------------- |
| `site:`     | Search within a specific domain    | `site:example.com`      |
| `inurl:`    | Search in URL                      | `inurl:admin`           |
| `intitle:`  | Search in page title               | `intitle:"index of"`    |
| `filetype:` | Search by file type                | `filetype:pdf`          |
| `intext:`   | Search inside page text            | `intext:"confidential"` |
| `link:`     | Pages that link to a specific site | `link:example.com`      |
| `cache:`    | View cached version of a site      | `cache:example.com`     |
| `ext:`      | Same as filetype                   | `ext:xls`               |

 ## Architecture 
 ```
+----------------------+
|   Attacker / Hacker  |
|   (Browser & Google) |
+----------+-----------+
           |
           | Google Dork Queries
           v
+---------------------------+
|       Google Search       |
+---------------------------+
           |
           | Indexed Public Content
           v
+---------------------------+
|   Target Websites / Data  |
| - Leaked files            |
| - Open directories        |
| - Sensitive info          |
+---------------------------+

```


# Output:

# SITE:

<img width="1905" height="1140" alt="image" src="https://github.com/user-attachments/assets/dea92193-f9f9-46b2-a5c4-9d835fa6cae0" />



# INURL:

<img width="1909" height="1152" alt="image" src="https://github.com/user-attachments/assets/3c2d8929-49e4-4dc0-9ad4-0c5e58b8fb3a" />


# INTITLE:

<img width="1909" height="1142" alt="image" src="https://github.com/user-attachments/assets/c2d2147a-12ad-43c3-a44e-6e3e2b13c30d" />




# FILETYPE:

<img width="1911" height="1146" alt="image" src="https://github.com/user-attachments/assets/469e6c8c-4011-41d9-95e5-3d1df9e4c468" />


# INTEXT

<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/4ade259f-17e7-4c29-8b23-89efb09fa611" />


# LINK

<img width="1909" height="1142" alt="image" src="https://github.com/user-attachments/assets/941df9cf-02ea-4aaf-9a4d-0f9a950a1e8a" />


# CACHE
<img width="1901" height="1147" alt="image" src="https://github.com/user-attachments/assets/530abee5-43e1-4388-914c-535912c7c31e" />


# EXT

<img width="1815" height="1120" alt="image" src="https://github.com/user-attachments/assets/9b667c4f-d4b9-473b-a882-3ce7548e435a" />



# DNS Enumeration
<img width="831" height="450" alt="image" src="https://github.com/user-attachments/assets/e7b2b5e6-65c7-4793-906e-1b8e2d12e66c" />



## DNS Recon

 provides the ability to perform:
 Check all NS records for zone transfers
 Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
 Perform common SRV Record Enumeration
 Top level domain expansion

<img width="998" height="491" alt="image" src="https://github.com/user-attachments/assets/2f453201-dc39-4dd3-a9e9-a2381fa4cb45" />



| Record Type | Meaning                        | Example Output                   |
| ----------- | ------------------------------ | -------------------------------- |
| A           | Host to IPv4 address           | `example.com -> 93.184.216.34`   |
| AAAA        | Host to IPv6 address           | `example.com -> ::1`             |
| MX          | Mail server info               | `mail.example.com`               |
| NS          | Name servers                   | `ns1.example.com`                |
| TXT         | Misc data (SPF, verifications) | `v=spf1 include:_spf.google.com` |
| CNAME       | Canonical names (aliases)      | `www -> example.com`             |

## Common Tools Used (Kali Linux)

| Tool           | Description                                | Usage Example                           |
| -------------- | ------------------------------------------ | --------------------------------------- |
| `nslookup`     | DNS lookup tool (simple queries)           | `nslookup example.com`                  |
| `dig`          | DNS lookup utility (detailed)              | `dig example.com any`                   |
| `host`         | Simple DNS querying tool                   | `host example.com`                      |
| `dnsenum`      | Perl script to enumerate DNS info          | `dnsenum example.com`                   |
| `fierce`       | DNS scanner to locate non-contiguous IPs   | `fierce -dns example.com`               |
| `dnsrecon`     | Powerful DNS enumeration script            | `dnsrecon -d example.com -a`            |
| `theHarvester` | Subdomain enumeration using search engines | `theHarvester -d example.com -b google` |


## OUTPUT:

# NSLOOKUP

<img width="752" height="812" alt="image" src="https://github.com/user-attachments/assets/4d09669d-a5d7-43e9-983a-b87b395dd52f" />

# DIG

<img width="726" height="564" alt="image" src="https://github.com/user-attachments/assets/fec89592-9804-48d2-91a5-5e5636741f9b" />

# HOST

<img width="750" height="447" alt="image" src="https://github.com/user-attachments/assets/67f39315-8ad0-4d37-8536-155e1731829d" />

# DNSENUM

<img width="733" height="543" alt="image" src="https://github.com/user-attachments/assets/7c1e5164-50a3-4edc-b3c2-f1d8fb7342f1" />

# DNSRECON

<img width="746" height="603" alt="image" src="https://github.com/user-attachments/assets/bb21a594-6fae-4950-9a29-98392372574c" />

# FIERCE 

<img width="742" height="762" alt="image" src="https://github.com/user-attachments/assets/3836a9af-37da-448a-ac8d-ae7fbbcee8dd" />

# Harvestor

<img width="739" height="705" alt="image" src="https://github.com/user-attachments/assets/f31dcc14-9a74-41ee-8ca0-b1bc96359f82" />

## Architecture Diagram 
```
+-------------------+        +------------------+       +------------------+
|                   |        |                  |       |                  |
|   Attacker (You)  +------->|   Target Server   +<----->+    DNS Server    |
| Kali Linux / Parrot|       | (Mail / DNS Host) |       |  (Authoritative) |
+---------+---------+        +---------+--------+       +---------+--------+
          |                            ^                          ^
          |                            |                          |
          |                            |                          |
          |           +-----------------------------+            |
          |           |      Information Tools      |            |
          |           |-----------------------------|            |
          |           | smtp-user-enum              |            |
          |           | nmap --script smtp-enum-*   |            |
          |           | dnsenum                     |<-----------+
          |           +-----------------------------+
          |
          v
+-----------------------------+
|   Output/Report             |
|  - Usernames Found          |
|  - MX Records / Zones       |
|  - Subdomains / IPs         |
+-----------------------------+

```

## dnsenum
**Purpose:** A multithreaded Perl script to enumerate information from DNS servers.

**Use case:** Performs DNS zone transfers, brute force subdomains, and gather host IPs.

```
dnsenum example.com
```

## Output:

<img width="736" height="510" alt="image" src="https://github.com/user-attachments/assets/95163872-8224-47b5-adeb-68db81607fb4" />



## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```
  
 ## Output
  
<img width="747" height="415" alt="image" src="https://github.com/user-attachments/assets/df055f43-0a50-48ec-ab9e-9e27218eef4d" />


## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:

<img width="680" height="142" alt="image" src="https://github.com/user-attachments/assets/bf2982f5-e7bb-4537-9a7d-bc5bfed15ad2" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
