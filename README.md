# nAPIs
 is a lightweight static analysis tool written in C++ designed to scan iOS application binaries (Mach-O files) for **network-related APIs** and **external server endpoints (URLs)**.  
This tool is ideal for mobile security researchers, reverse engineers, and bug bounty hunters who want to identify potential API connections and backend servers used by an iOS app — **without executing the application.**

Author:Abdulrahman AL-Hakami

---


-  Extracts **network communication APIs** such as:
  - `NSURLSession`
  - `CFNetwork`
  - `NSURLRequest`, `NSMutableURLRequest`
  - Third-party libraries like `Alamofire`, `AFNetworking`

- Identifies **hardcoded external URLs/domains**
  - Example: `https://api.example.com/login`
  - Helps detect suspicious or insecure HTTP endpoints

-Performs lightweight static string extraction from Mach-O binary files

-No dynamic execution required (purely static and offline)

---

##  Usage

```bash
./nAPIs <path_to_MachO_binary>
