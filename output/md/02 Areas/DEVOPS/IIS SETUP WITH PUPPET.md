---
tags:
- PUPPET
---
   
**#IIS**    
   
     
   
     
   
IIS (Internet Information Services) is a web server from Microsoft that runs on Windows systems. IIS is easy to set up and configure and can be used to host websites and web applications. IIS can also be used to host FTP sites and serve as a reverse proxy server.   
   
     
   
@TO ALLOW THE PERMISSIONS OF 500.19 ERROR    
   
@create a authentication users in the edit permissions section and add it to resolve the issue   
   
     
   
I have setup the IIS server by adding the roles and the features as per need and also I have setup the Z credentials of the the users and giving the authorisation to the specif users.   
   
     
   
also I have setup folders, apps, sites ,bindings, pools in the IIS manually for many servers   
   
     
   
Additionally we also can use `{_obsidian_pattern_tag_PUPPET}`  scripting to setup the servers by coding, so that we don’t need to add those addtional things manually on each server.   
   
     
   
**Overview Example Class:**   
   
Before diving into the weeds in each section, I wanted to provide a code sample of a single application pool, website, virtual directory, and web application, complete with the DSC dependencies:   
   
     
   
example with code    
   
[https://www.metaltoad.com/blog/managing-iis-configuration-puppet-powershell-dsc](https://www.metaltoad.com/blog/managing-iis-configuration-puppet-powershell-dsc)   
   
     
   
     
   
MANAGING WINDOWS WITH PUPPET     
   
another example with code   
   
     
   
[https://www.ipswitch.com/blog/managing-windows-with-puppet](https://www.ipswitch.com/blog/managing-windows-with-puppet)