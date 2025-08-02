# Decoding the Internet’s Phonebook: Understanding DNS

![My Image](./media%20files/DNS/d507966a-5fe0-4450-9ba9-3cc9d6de5ad6.webp)

## 🌐What is DNS?
DNS (Domain Name System) is a system that lets us use human-friendly names (like google.com) instead of having to remember complex IP addresses (like 142.250.67.78).

When you type a URL like www.youtube.com into your browser, it seems like magic that the website just loads instantly, right? But have you ever wondered how your computer knows where to find that site?

Your computer doesn’t actually understand website names like youtube.com. What it really needs is an IP address a unique number that tells it where the website lives on the internet 🌍.

That’s where DNS servers come in! 🖥️

They translate human-friendly names (like youtube.com) into machine-friendly IP addresses (like 142.250.64.78). It's just like how you'd look up a contact's name in your phone and it dials the correct number for you.

## 📝Domain Names Decoded: How to Own One and Trace Its IP
Domain names are human-readable, unique web addresses (like example.com) that correspond to specific IP addresses the numerical identifiers used by computers to locate and communicate with each other over the internet.

These are some domain names along with their corresponding IP addresses. Please note that these IPs are only examples and may change over time.

| **Domain Name**	| **IP address (example)**|
|-------------------|---------------------|
|google.com         |	142.250.192.14    |
|youtube.com	    |   142.250.195.206   |
|amazon.com         |   176.32.103.205    |
|microsoft.com      |	40.113.200.201    |
---

## How to get your own domain name?
1. Choose a domain name Pick something short, easy to remember, and relevant to your website.

2. Check availability Visit a domain registrar like GoDaddy, Namecheap, or Google Domains to see if your desired name is available.

3. Create an account with the registrar If the domain is available, sign up with the registrar and choose the registration duration.

4. Make the payment Complete the purchase by paying the required fee.

5. Connect your domain to your hosting provider If you're building a website, link your domain to your web hosting service using the DNS settings provided.

## 💡 How to See a Website’s IP Address on Your Computer
1. Open the Terminal On Windows, you can use Command Prompt or PowerShell. On macOS or Linux, open the Terminal app.

2. Type the following command:

   > nslookup google.com 

   Replace google.com with the domain name you want to look up.

3. Press Enter The command will query the DNS server.

4. Result: you will see IP address of the domain listed under Non-authoritative answer.

## 🖥️DNS Servers
When you type a URL into your browser, your browser sends a query to a DNS server. The DNS server translates the human-friendly domain name (like google.com) into a computer-friendly IP address so your device knows where to go. This process is called DNS resolution.

Most of the time, your Internet Service Provider (ISP) automatically assigns you a DNS server. These are called default resolvers. But you’re not stuck with them—you can switch to a faster or more privacy-focused DNS service, like Google DNS or Cloudflare DNS, for better speed and security.

## 🌍DNS Hierarchy Explained: Root to Authoritative Servers
| Server | Functions|
|--------|----------|
|🔄 Recursive Resolver|	takes browser's domain request and perform all the work to find the IP address of the site. It often catches up the result for future lookups. (your DNS helper)|
|🔝 Root DNS Servers|	They don’t know exact IP addresses, but they do know where to find the servers that do it's the starting point of the DNS lookup it replies with the address of the correct TLD server (like .com, .org, etc.).|
|🏷️ Top-Level Domain (TLD) Servers|	Handles domain extensions like .com, .net, .in, etc. It tells the resolver where to find the Authoritative Name Server for the specific domain (like google.com under .com)|
|📁 Authoritative Name Servers|	These are the final stop! They store the actual IP address for the domain you're looking for. When you want to visit example.com, this server says, “Here’s where it lives: 93.184.216.34.”|

--- 
### DNS Lookup Flow:
![My Image](./media%20files/DNS/b8a76848-5d34-46ff-89c3-7ac4da134cde.jpeg)

```

1. Browser -> DNS Resolver: "What is the IP of www.example.com?"

2. Resolver -> Root Server: "Where can I find .com domains?"
            ↳ Response: "Ask the .com TLD server at IP x.x.x.x"

3. Resolver -> TLD Server (.com): "Where is example.com?"
            ↳ Response: "Ask authoritative server at IP y.y.y.y"

4. Resolver -> Authoritative Server: "What is the IP of www.example.com?"
            ↳ Response: "The IP is z.z.z.z"

5.Resolver -> User: "The IP of www.example.com is z.z.z.z
```


--- 
## 🙌 Final Thoughts

That’s a wrap on DNS! 🎉 Now you know how websites get their digital directions and how the internet finds its way. Thanks for reading!

> **"Behind every click is a system that makes it happen—understand it, and you control it. 💻⚡**

### 🔗 Explore More on My Hashnode Blog

Check out more articles and insights on my [Hashnode website](https://codealpha.hashnode.dev/).
