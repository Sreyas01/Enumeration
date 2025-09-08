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

<<img width="586" height="776" alt="image" src="https://github.com/user-attachments/assets/022ae630-a356-4a42-a950-8cbce17e873a" />


# DIG

<img width="632" height="353" alt="image" src="https://github.com/user-attachments/assets/3f2024b0-1279-409b-ab81-39855c673374" />


# HOST

<img width="667" height="404" alt="image" src="https://github.com/user-attachments/assets/d6df56ec-809a-49b3-8ba5-0acefeae09e9" />


# DNSENUM

<img width="667" height="404" alt="image" src="https://github.com/user-attachments/assets/1b42ec82-e7b2-45aa-a721-941318005379" />


# DNSRECON

<img width="695" height="500" alt="image" src="https://github.com/user-attachments/assets/93178ddf-4d2d-405c-9f19-924fa71feb37" />


# FIERCE 

<img width="742" height="762" alt="image" src="https://github.com/user-attachments/assets/3836a9af-37da-448a-ac8d-ae7fbbcee8dd" />

# Harvestor

<img width="615" height="325" alt="image" src="https://github.com/user-attachments/assets/57e466b5-e9f3-42eb-b954-d273576b8338" />


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

<img width="801" height="446" alt="image" src="https://github.com/user-attachments/assets/bd54bb6f-4908-4817-963d-03cfcea4f643" />




## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```
  
 ## Output
  
<img width="693" height="368" alt="image" src="https://github.com/user-attachments/assets/5d75dd42-ecc8-496c-9d7c-c9b65599edce" />



## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:

<img width="602" height="177" alt="image" src="https://github.com/user-attachments/assets/ed2f2726-cfd1-44d4-a3e5-29cdb4c54637" />



## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
